# Mercury: A Daily Blog Agent With a Mandate and a Quality Gate

Remya Narayanankutty | Founder and CEO, Belong India

## The problem
Daily, useful content compounds into search traffic, but a founder with limited weekly hours cannot write and publish it by hand. The risk of handing it to an AI is just as real: a post under the brand's name that is wrong, duplicated or off-brand is worse than no post.

## What I built
One agent with one job: publish one SEO blog post a day to the store's blog. It is defined by five things.
- **A definition:** who it is, its tools, who it reports to, and its non-negotiables.
- **A mandate:** mission, objectives, audience, voice, hard rules and an SEO spec. Only I change it.
- **A procedure:** an eight-step skill it follows on every run.
- **State files:** a topic queue and a log of what it published, because the agent forgets everything between runs.
- **A strategy:** written and owned by the agent, reviewed monthly.

## How it works
Each run starts cold and follows the same path:
1. Load the mandate, queue, log and my notes.
2. Pull the live blog's recent titles, as the authoritative check for duplicates.
3. Choose the topic from the strategy and the season.
4. Verify every fact and confirm every internal link points to a page that exists.
5. Write to spec: an answer first, questions as headings, a short FAQ, and matching structured data.
6. Run the quality gate.
7. Publish live, or save as a hidden draft if any check fails.
8. Record the result and commit it, so the next run knows what shipped.

The hard rules are plain: no invented statistics, studies or quotes, no health claims, no competitors, local sizing and seasons only, and no two posts in a day.

## What went wrong and what I changed
- Mercury's first definition said to publish on every run, so opening a chat with it would have published a second post. I split it into work mode and conversation mode.
- Agents forget between sessions, so guidance from a conversation was lost. I added a notes file that the agent reads on every run and writes to at the end of every conversation.
- Mercury cannot measure everything its objectives need, such as search-console clicks. It now lists the data it needs, and the chief-of-staff agent supplies it before each review.

## How AI was used
- **Pattern:** A scheduled agent that follows a written procedure and keeps its memory in files, plus a monthly loop in which it reviews its own results.
- **Autonomy:** High for routine work. It publishes live without a per-post approver, and falls back to a hidden draft when any check fails.
- **Guardrails:** Least-access tools: it can write blog articles and read the store, but cannot touch products, prices, the theme, customer data or email. It checks the live blog for duplicates and verifies links before publishing. If anything upstream is broken, it logs the failure and stops.
- **Human checkpoints:** I own the mandate. In conversation mode the agent discusses and drafts but never publishes unless I say so. A one-line notification follows each live post, and I spot-check output.
- **How it improved:** Two modes after the double-post risk, a notes file for memory, a monthly strategy cycle, and a data request list for what it cannot measure itself.
- **My role:** I set the mission, the hard rules and the agent's access, and I decide what changes in the mandate.

## The monthly strategy cycle
The agent writes three to five testable bets, each with a metric and a date to check. After 30 days it gives each bet a verdict: keep, tweak or drop. It may make at most two changes per cycle, so results stay attributable, and it separates its own effect from outside factors such as price, email and season. Anything blocking an outcome that is outside its lane goes into a list of asks for me, and it does not act on them.

## What I would do next
Run the first full monthly review and add the verdicts to this page as trends.
