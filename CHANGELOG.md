# Changelog

How the agent team has progressed, newest first. Each entry says what changed, why, and what I learned. Results appear only when they are meaningful, and then as trends or ratios.

## 2026-10-29: Stories switch on by rule
**What changed:** Venus began publishing a Story of each post, switching itself on once its own conditions were met: two clean posts on both platforms, a clean reel, no failures in three days, and no pause file.
**Why:** Stories show a post to existing followers in the first hours, which helps a small account. A rule the agent checks itself kept the reel test clean, because a new feature did not start on the same day.
**Learned:** Letting an agent decide when to enable a feature works if the conditions are explicit and checkable.

## 2026-10-27: Capabilities restricted in code, and the first supervised post
**What changed:** Venus's image upload script was cut down to file staging only, with no other store access. The first post went out supervised. Instagram rejected every image link from the store's content network, so I moved image staging onto Meta's own infrastructure. A design-tool test returned a blank page, so slides are now rendered locally from a spec.
**Why:** Limiting a capability in the script keeps the damage small even if an instruction is misread. Testing found the image failure was on the fetch side, so the fix moved the image to where the platform could read it.
**Learned:** Restrict access in code, not only in instructions, and test the full path before turning on automation.

## 2026-10-26: Reels as a tested format
**What changed:** Venus began building silent reels from its carousel slides, capped at half of all posts until a test shows they win.
**Why:** Reels reach non-followers more than carousels, but there was no evidence for a silent slideshow on a small account. So it is tested, not assumed. Silent only, because licensed audio cannot be added through the API.
**Learned:** Treat a plausible format as a hypothesis with a stopping rule.

## 2026-10-25: Venus, an autonomous social agent with no per-post approver
**What changed:** A second agent was created to ideate, design, publish and measure one Instagram and Facebook post a day, learning through a weekly playbook loop and a monthly strategy review.
**Why:** Without an approver, guardrails had to do the approver's job: hard rules in the mandate, an automated quality gate, a publish script that rejects duplicates and over-cap posts, and a one-file kill switch.
**Learned:** The more autonomy an agent has, the more of its safety must be enforced outside its own judgment.

## 2026-10-10: Monthly strategy cycle
**What changed:** Each agent writes its own strategy as three to five testable bets, works to it for 30 days, gives each bet a verdict, and makes at most two changes before the next cycle.
**Why:** Capping changes at two keeps results attributable. Keeping strategy separate from the mandate lets the agent adapt its approach without touching the rules I own.
**Learned:** Separate what must be achieved, which stays with the founder, from how to achieve it, which belongs to the agent.

## 2026-10-10: An org standard for agents
**What changed:** Every agent now has a definition, a mandate, state files and a notes file, plus two modes: work mode for delegated runs and conversation mode for one-on-ones, where it discusses and drafts but takes no action unless asked.
**Why:** Mercury's first definition told it to publish on every run, so opening a chat with it would have published a second post. Agents forget between sessions, so guidance has to live in a file they read each run.
**Learned:** Design the interaction modes up front, and make memory a file, not an assumption.

## 2026-10-09: Mercury, the daily blog agent
**What changed:** The first agent went live: one SEO blog post a day, written to a mandate with hard rules, a quality gate, and a fallback to a hidden draft when a check fails.
**Why:** A reliable daily cadence compounds, and a founder with limited weekly hours cannot supply it by hand.
**Learned:** A missed day is acceptable. A broken or duplicate post is not.

## 2026-06: A measurement framework with one trusted metric
**What changed:** I made visits from the target market the primary metric, added a tagging standard for every external link, and built a weekly tracker with a checkout health monitor.
**Why:** Total traffic was inflated by crawlers and non-target visitors, and untagged email links were counted as direct visits.
**Learned:** A dashboard that measures the wrong thing changes every decision after it.

## 2026-06: A reusable homepage update skill
**What changed:** Banner refreshes became a trigger-based skill that takes a short spec and produces a reviewed draft for a one-click publish.
**Why:** Compressing images, editing the theme and checking the result is repetitive work that a founder with limited weekly hours should not do by hand.
**Learned:** Match blocks by type, not by ID, and judge each banner on the device most visitors use.

## 2026-06: Size-aware merchandising
**What changed:** Size collection pages and product pages now show the right dimensions, and a script removes per-size sold-out items.
**Why:** Fit and stock are per size, so a static note shows wrong information.
**Learned:** Research the local term before you name a product, because a name that works elsewhere may not sell here.

## 2026-06: A safe change workflow for the live store
**What changed:** Every theme change now follows the same loop: duplicate, edit the draft, verify, publish on approval, and commit. The theme code is under version control, and an unused app was removed only after proving nothing depended on it.
**Why:** A mistake on a live store costs sales, and the first access attempt failed three times for the same reason.
**Learned:** Write the recipe down the first time it works.

## 2026-05: A site-speed pass over every product image
**What changed:** I audited every product image, then ran a resumable pipeline that downloads each oversized image, compresses and resizes it, re-uploads it with its image text, and removes the old one. Follow-up scripts restored image order and colour links.
**Why:** Most visitors are on phones, and multi-megabyte photos were the main cause of slow product pages. Doing hundreds by hand was not realistic.
**Learned:** Replacing an asset has side effects, so plan the clean-up before you run the batch.

## 2026-05: A structured-data layer
**What changed:** I shipped organization, product, breadcrumb and social-sharing markup as small reusable snippets, validated on a draft before publishing.
**Why:** Search engines and AI tools needed clean signals, and the homepage had no true main heading.
**Learned:** Keep each concern in its own small file, so later updates are safe.

## 2026-04: SEO foundations
**What changed:** I fixed headings, titles and descriptions, wrote descriptive image text in batches, and removed leftover content and metadata from a previous business.
**Why:** Inconsistent terminology and keyword-stuffed copy muddied what the store was about.
**Learned:** Settle one terminology rule from how customers search, then apply it everywhere, including hidden fields.
