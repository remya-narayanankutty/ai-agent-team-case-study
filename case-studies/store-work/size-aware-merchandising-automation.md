# Size-Aware Merchandising, Automated

Remya Narayanankutty | Founder and CEO, Belong India

## The problem
Bedding buyers hesitate over one question: will it fit my bed? In this store, fit and stock are per size, not per product. A static note would show the wrong dimensions or list items that were sold out in that size. The shopper's frustration with sold-out items and the missing fitted sheets on one size page both stalled purchases, and most visitors were on mobile.

## What I built
- A size-aware block on each size collection page that shows the right dimensions and an audience tag only where it applies.
- A four-size table on every bedsheet product page, placed right after the buy button and shown only for products with a size option.
- A reusable script that removes per-size sold-out items from each size collection, so shoppers only see what they can buy.
- Fitted sheets added to the size page that had none, paired with flat sheets by colour.

## How it works
- **Handle-scoped, not per-file.** All size pages share one template, so the logic keys off the collection and the variant, not a separate file for each.
- **Draft, preview, publish.** Every edit was made on a draft theme and previewed before I published it.
- **Naming by market.** I researched the wider size and found the right Indian term, which is a recognised local word. The term the store had been using is common in other regions and does not resonate in India, which is why it never sold. I renamed it across the catalogue.

## What went wrong and what I changed
- A non-standard size had no collection and did not sell. I parked it, rather than force it into the structure.
- A pillow-count contradiction in one description and a few inconsistent labels were caught and fixed during review.

## How AI was used
- **Pattern:** AI-built tools in a gated rollout. Reusable scripts do the repeatable parts.
- **Autonomy:** The AI builds and runs the scripts on drafts. The sold-out pruning script can be run again whenever stock changes.
- **Guardrails:** Draft, preview and publish. Blocks render only where they apply, such as a size table only on products with a size option. Logic is per size, not per product, so nothing shows wrong information.
- **Human checkpoints:** I review each change on the draft before approving the publish.
- **How it improved:** I adjusted the box position and the copy after seeing it on the page, and a non-standard size was parked.
- **My role:** I set the goal and ruled that sold-out items be removed per size.

## Results
The size pages now show only what is buyable, the product pages answer the fit question up front, and the sold-out pruning is a one-command routine. Conversion effects will be added as trends once the data supports them.

## What I would do next
A two-way sync that also re-adds items when they are restocked, run weekly.
