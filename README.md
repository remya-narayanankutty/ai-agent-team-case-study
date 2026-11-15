# Running a D2C Brand with a Team of AI Agents

Remya Narayanankutty | Founder and CEO, Belong India

## The problem

Belong India is a direct-to-consumer bedding brand serving shoppers in India. The business is profitable and runs on a small team, but its organic reach was small, and growth had to come without paid marketing. Content and social media are the two levers that compound over time, and both need daily consistency that a founder with limited weekly hours cannot supply by hand.

I treated it as a management problem, not a tooling problem. The question was how to hand daily content and social work to AI agents and still stay accountable for everything published under the brand's name.

## What I built

A small org of agents with clear reporting lines, built on Claude Code:

- **Mercury** writes and publishes one SEO blog post a day.
- **Venus** designs, publishes and measures one Instagram and Facebook post a day, and learns from the numbers.
- **Cospian Dave**, a chief of staff agent, triggers the others, reviews their output and briefs me.

Every agent has the same five parts: a definition, a mandate that only I can change, state files so each run knows what already happened, a notes file for my guidance, and a strategy the agent writes and owns. I can talk to any agent one-on-one. In that mode it discusses and drafts but takes no action unless I explicitly ask.

## Guardrails

Venus publishes with no per-post approver, so the rules had to be strong enough to stand in for one. They are enforced in code where possible, not only in instructions:

- The publish script rejects captions containing banned punctuation, duplicate captions, and posts over the daily cap.
- A single `PAUSE` file stops all publishing instantly.
- Venus's only store capability is uploading its own post images. The script contains only those calls, so a misread instruction cannot reach anything else.
- Each agent has a quality gate. If it fails and cannot be fixed, the agent skips the day or saves a hidden draft. A missed day beats a bad post.
- Agents may not invent statistics, testimonials or discounts, make health claims, or name competitors.

## How the agents learn

I set the outcomes. The agents decide how to reach them.

- **Monthly strategy cycle.** Each agent pulls a baseline, writes 3 to 5 testable bets, works to them for 30 days, then gives each bet a verdict: keep, tweak or drop. It may make at most two changes per cycle, so results stay attributable.
- **Weekly learning loop (Venus).** Every post is scored, with shares and saves weighted above likes. Tests run one variable at a time, with at least 4 posts per arm. A variant wins only if its median beats the other by 25% and at least 3 of 4 posts beat the other arm's median. Otherwise the verdict is "no difference yet".
- **Honesty rules.** No number is used unless a command produced it. Unavailable metrics are written as unavailable.

## What went wrong and what I changed

- Mercury's first definition told it to publish on every run, so opening a chat with it would have published a second post. I split each agent into work mode and conversation mode.
- Canva's design tool returned a blank page for carousels. Venus now renders slides locally from a spec, which is deterministic and repeatable.
- Instagram rejected every image link from the store's CDN. I traced it to the fetch side and moved image staging onto Meta's own infrastructure.

## Who decided what

I made the strategic calls: the mission, the objectives, the guardrails, which capabilities each agent gets, and when to turn a format on. The agents execute inside those limits, run their own experiments, and report to me. Every agent's output goes out under the brand's name, so I spot-check it.

