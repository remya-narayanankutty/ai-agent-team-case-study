# A Reusable Skill for Homepage Updates

Remya Narayanankutty | Founder and CEO, Belong India

## The problem
The homepage banner is the most valuable space on the site, and it should change with a sale, a season or a launch. Each refresh meant a fresh round of image compression, theme editing and checking, which is exactly the repetitive work that eats a founder's limited weekly time.

## What I built
A trigger-based skill, not a weekly chore. When a sale starts or ends, a season turns or a clearly better message is ready, I describe the new banner in a short spec: image, headline, subtext and button. The skill then does the rest:
1. Compress the image and upload it.
2. Duplicate the live theme.
3. Edit the top banner on the draft.
4. Verify the result.
5. Stage it for a one-click publish.

## How it works
- **Spec-driven.** The same engine handles every refresh, because only the inputs change.
- **Blocks matched by type, not by ID.** Banner blocks are found by what they are, because their IDs change from one theme copy to the next.
- **Mobile first.** Most visitors are on phones, so I judged each banner on mobile and accepted a version that was good enough on desktop. When a text box covered the subject on desktop, I shortened the headline and recentred it.
- **Truthful claims.** A banner aimed at one audience used a softer, accurate phrase for the cotton, and the brand-wide line stayed unchanged. The rule is never to imply a certification the brand does not hold.

## What went wrong and what I changed
- The first banner hid the subject on desktop. Checking the device split drove the redesign.
- Publishing is gated on my explicit approval, because it is a public change.

## How AI was used
- **Pattern:** A reusable skill: a named, trigger-based workflow driven by a short spec.
- **Autonomy:** End to end up to a staged draft. It stops before publishing.
- **Guardrails:** Publishing is gated on my approval. Blocks are matched by type, not ID. A truthfulness rule stops claims the brand cannot support.
- **Human checkpoints:** I review the staged banner and approve the publish.
- **How it improved:** The first banner hid its subject on desktop, so the headline was shortened and recentred after checking the device split.
- **My role:** I choose the angle and approve each publish.

## Results
A banner refresh went from a multi-step chore to one command with an approval at the end. Impact on click-through and sales will be added as a trend once the data supports it.

## What I would do next
Add a checklist that reverts the banner automatically when a sale ends.
