# Structured Data and Technical SEO, Shipped Safely

Remya Narayanankutty | Founder and CEO, Belong India

## The problem
A direct-to-consumer store needed to be understood by search engines and AI tools, but its homepage had no true main heading, its pages carried weak structured data, and leftover metadata from a previous business muddied its topic. All of this had to be fixed without editing the live store and without paid help.

## What I built
A structured-data layer for the whole store, delivered as small, reusable theme snippets rather than one large file:
- Organization and WebSite markup, with social profiles and the areas the brand serves.
- Product markup that covers every variant and offer.
- Breadcrumb markup for product, collection and blog pages.
- Ratings markup, switched on through the reviews app, with no custom code.
- Social sharing tags for every page.

## How it works
- **Draft first.** Every change was made on a duplicate of the live theme, never on the live one. I audited the schema through the store connector, built the snippets on the draft, and validated them with Google's rich results test before anything went live.
- **Small files.** Keeping product markup in its own snippet means future updates, such as a yearly validity date, can be made safely with no risk of file-size problems.
- **Consolidation.** Two drafts that each branch from the live theme overwrite each other on publish, so all changes were merged into one draft first.

## What went wrong and what I changed
- The homepage hero image had no true H1. Fixing it in the template, not in content, fixed it for every future refresh.
- A previous business had left its metadata on the blog page. A site-wide audit showed the catalogue itself was clean, so the fix was small and targeted.

## How AI was used
- **Pattern:** A supervised workflow. The AI audits, drafts and validates. It does not decide what ships.
- **Autonomy:** Medium. It reads the live theme and writes to drafts only.
- **Guardrails:** Writes go only to a duplicate of the live theme, which the store connector enforces. Every change is checked with Google's rich results test before it counts as ready.
- **Human checkpoints:** I approve the publish. A few theme-editor edits the connector could not make, I made myself.
- **How it improved:** After finding that two drafts overwrite each other on publish, I consolidated changes into one draft first. Product markup moved into its own snippet so later changes are safe.
- **My role:** I set the priorities and approved every publish.

## Results
Validation passed with no errors on the rich results test. Search-visibility results will be added only as trends once the data is meaningful.

## What I would do next
Add ratings markup for the shopping surfaces once there are enough reviews, and keep the schema under the same review loop as the theme.
