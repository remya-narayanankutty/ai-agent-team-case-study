# On-Page SEO at Scale, Through the Store API

Remya Narayanankutty | Founder and CEO, Belong India

## The problem
A catalogue of over a hundred variants and dozens of collections had inconsistent titles, thin or keyword-stuffed descriptions, and image text that did not describe the images. Fixing it by hand in the admin would have taken far more of my limited weekly time than the work was worth.

## What I built
A repeatable audit-and-fix routine run through the store's API:
- A full audit of every collection, product, page and blog.
- Rewrites of weak or keyword-stuffed descriptions into concise, accurate copy.
- Descriptive, consistent image text across all product and blog images, in batches.
- Consistent terminology everywhere, driven by how Indian shoppers actually search.

## How it works
- **One rule, applied everywhere.** I fixed the brand's terminology once, based on how customers search. Titles, product fields, image text and the homepage were then brought into line with that rule, including places the admin does not make obvious, such as a custom product field.
- **Audit, then fix.** A scan lists everything that breaks the rule. A script fixes it in batches, and a second scan confirms nothing is left.
- **Judgement on top of automation.** I kept a collection that looked redundant, because it matched a term shoppers genuinely use. I also decided against stuffing the brand name into every image text, because it reads as over-optimisation.

## What went wrong and what I changed
- Old terminology survived in fields no audit of titles would catch: a product subtitle on every page, and several product names. Scanning every field, not just the obvious ones, found them.
- The homepage title is not exposed through the API, so I verified it on the live page instead of assuming.

## How AI was used
- **Pattern:** An audit-and-fix loop: scan, fix in batches, scan again, until nothing breaks the rule.
- **Autonomy:** Medium. The AI drafts copy and runs batch updates through the store API.
- **Guardrails:** One terminology rule applied everywhere, batches logged and re-checked, and judgement calls, such as which collection to keep, left to me.
- **Human checkpoints:** I approve the copy and the rules before changes go live.
- **How it improved:** The first scan missed a hidden product field, so the audit now checks every field, not only titles.
- **My role:** I set the terminology rule and the limits on optimisation.

## Results
The audit and fix are complete. Search results will be added as trends once there is enough data to be meaningful.

## What I would do next
Re-run the audit after each catalogue change, so inconsistencies never build up again.
