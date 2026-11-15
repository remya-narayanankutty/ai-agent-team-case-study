# Venus: An Autonomous Social Agent That Learns From Its Own Results

Remya Narayanankutty | Founder and CEO, Belong India

## The problem
The brand needed a daily social presence on Instagram and Facebook, with no social team and no paid promotion. Posting publicly without a reviewer carries a real risk: one bad post can damage an account that took time to build. At the same time, a small account produces noisy data, so it is easy to fool yourself about what works.

## What I built
One agent that ideates, designs, publishes and measures one post a day, and improves from the numbers.
- **Formats:** carousels by default, reels and stories as tested additions.
- **Creation:** hooks first, then a short script, then slides rendered locally from a spec using the brand's own product photos.
- **Publishing:** a script that posts to both platforms through the platform API.
- **Learning:** every post is scored and tagged, a weekly playbook records what works, and a monthly review checks the strategy.

## How it works
Each run follows the same path: check for a pause file and for a post already published today, measure recent results, run any due learning review, pick an idea, create it, run the quality gate, publish, then record and commit. The agent skips the day if a gate fails and cannot be fixed.

**The learning loop is designed to avoid self-deception.**
- Shares and saves count for more than likes in the score, because they carry a post to new people. The score is divided by reach, so posts are comparable.
- Only one variable is tested at a time, with at least four posts per arm.
- A winner needs a median at least a quarter higher and at least three of four posts ahead. Otherwise the verdict is "no difference yet".
- About 70 percent of posts use what works, and about 30 percent explore on purpose.
- The agent never states a number it did not measure. If a metric is unavailable, it says so.

## What went wrong and what I changed
- The design tool returned a blank page for carousels, so slides are now rendered locally from a spec, which is deterministic and repeatable.
- Instagram rejected every image link from the store's content network. Testing showed it was a fetch problem on the platform side, so images are staged on the platform's own infrastructure.
- The first post went out supervised, so the full path was proven before automation.
- Reels and stories were added only as tests with stopping rules, not assumed to work.

## How AI was used
- **Pattern:** An autonomous agent with two loops: a weekly tactical loop that updates a playbook, and a monthly strategic loop that reviews its bets.
- **Autonomy:** High. There is no approver for individual posts, so the agent decides, publishes and measures on its own, and skips the day when a gate fails.
- **Guardrails:** Hard rules in the mandate (no invented evidence, testimonials or numbers, no health claims, no engagement bait, no unlicensed images or audio). An automated quality gate. A publish script that rejects duplicate captions, posts over the daily cap and banned punctuation. A one-file kill switch. Least access: it can post and measure, but cannot reply, run ads, message anyone or change store data, apart from an upload script that can do nothing else. Secrets are never printed or committed.
- **Human checkpoints:** I own the mandate and can stop everything instantly with the kill switch. I review results, not individual posts, and I switch features on by writing them into the mandate.
- **How it improved:** A local slide renderer after the design tool failed, a new image route after the platform rejected store links, reels added under a stopping rule, and stories that switch on by conditions the agent checks itself.
- **My role:** I set the mission, the guardrails and the agent's access, and decide which formats are allowed.

## What I would do next
Let the first controlled test finish, then add the verdict to this page as a trend.
