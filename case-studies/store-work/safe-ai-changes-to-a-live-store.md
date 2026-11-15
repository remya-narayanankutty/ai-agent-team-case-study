# Letting AI Change a Live Store Safely

Remya Narayanankutty | Founder and CEO, Belong India

## The problem
I wanted an AI assistant to make real changes to the store's theme, but a mistake on a live store costs sales. The store's connector blocks writes to the live theme by design, and my access token initially could not read or write theme files at all.

## What I built
A change workflow that makes risky edits safe, plus the plumbing to run it:
1. Duplicate the live theme.
2. Make every edit on the draft only.
3. Re-read the draft and validate it.
4. Publish only on my explicit approval, because it is a public-facing change.
5. Pull the published theme back and commit it, so each commit equals exactly what changed.

## How it works
- **Access, fixed once.** Extending the token's permissions failed through the obvious route, which redirects to a page that does not exist locally. The working route is a small local listener that catches the authorisation callback. I documented the recipe, so it takes minutes the next time.
- **Version control.** The theme code was not under version control at all. I mirrored it into a repository, so every future change has a diff and can be rolled back.
- **Secrets.** The access token was one careless command away from being committed. I added it to the ignore list and checked that it was ignored.
- **Proof before removal.** I removed an unused page-builder app only after proving nothing live depended on it: no page used its templates and it loaded no scripts. Then I deleted its leftover files from a draft, published, and verified the pages still rendered.

## What went wrong and what I changed
- The same access trap was hit three times across sessions before I wrote the recipe down.
- A freshly duplicated theme fills in a moment after it is created, so reads now retry.
- Two drafts branched from the live theme overwrite each other on publish, so changes are consolidated into one draft first.

## How AI was used
- **Pattern:** A gated workflow that makes AI changes safe: duplicate, edit, verify, publish, commit.
- **Autonomy:** The AI edits drafts freely. It never publishes on its own.
- **Guardrails:** The connector blocks writes to the live theme. Edits go to a draft only. Each draft is re-read and validated. Secrets are excluded from version control. Deletions need proof that nothing depends on the item.
- **Human checkpoints:** I approve every publish and every deletion.
- **How it improved:** After the same access problem hit three times, I wrote the working recipe down. Retries and consolidation rules were added as gotchas appeared.
- **My role:** I approve each publish and each deletion.

## Results
Every theme change is now auditable and reversible. The cleanup removed clutter without any visible speed change, which confirmed the app had already been dormant.

## What I would do next
Add a weekly check that pulls the live theme and flags any change made outside this workflow.
