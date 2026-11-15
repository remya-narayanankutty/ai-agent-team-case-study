# An AI Agent Team: The Operating Model

Remya Narayanankutty | Founder and CEO, Belong India

## The problem
Belong India is a direct-to-consumer bedding brand serving shoppers in India. The business runs on a small team, its organic reach was small, and growth had to come without paid marketing. Content and social media compound over time, and both need daily consistency that a founder with limited weekly hours cannot supply by hand.

I treated it as a management problem, not a tooling problem. The question was how to hand daily work to AI agents and still stay accountable for everything published under the brand's name.

## What I built
A small org with clear reporting lines, built on Claude Code:

```
Founder
└── Cospian Dave (chief of staff agent)
    ├── Mercury (daily blog)
    └── Venus (daily social)
```

- **Cospian Dave** triggers the others, reviews their output and briefs me.
- **Mercury** and **Venus** each own one job. Their case studies are linked below.

## The standard every agent follows
Each agent has the same five parts, so a new agent is a copy of a working pattern, not a fresh design:
1. **Definition:** who it is, its tools, who it reports to, its two modes and its non-negotiables.
2. **Mandate:** mission, outcomes, hard rules and a dated change log. Only I change it.
3. **State:** queue and log files, because agents forget between sessions.
4. **Notes from me:** read at the start of every run, written to at the end of every conversation.
5. **Strategy:** written and owned by the agent, not by me.

**Two modes.** In work mode an agent does its job. In conversation mode I can talk to it one-on-one: it answers, discusses and drafts, but takes no action unless I explicitly ask. I added this after finding that opening a chat with Mercury would have published a second post.

## The strategy cycle
I decide what must be achieved. The agent decides how. It sets a baseline, places three to five testable bets, works to them for a month, gives each a verdict, and makes at most two changes. Anything blocking an outcome that is outside its lane goes to me as an ask, and it does not act on it.

## Rules for the whole org
- One job per agent. An agent declines work outside its role.
- Least access. Each agent gets only the tools its job needs.
- Files are memory. If it is not written down and committed, it did not happen.
- Fail safe. When something upstream is broken, an agent logs it and stops. A missed day beats a broken output.
- The founder is accountable. Everything an agent publishes goes out under the brand's name, so output is spot-checked.

## How AI was used
- **Pattern:** A supervised org of autonomous agents. A chief-of-staff agent supervises, and each agent runs on a schedule with its own memory in files.
- **Autonomy:** High for routine work, bounded by mandates and access limits.
- **Guardrails:** Mandates with hard rules, automated quality gates, checks enforced in code rather than in instructions, and least-access tools.
- **Human checkpoints:** I own every mandate, review results, spot-check output, and can pause the whole system.
- **How it improved:** Each agent started as a copy of the first, and each failure became a rule in the standard.
- **My role:** I set the mission, the guardrails and each agent's access.

## The agents
- [Mercury: the daily blog agent](mercury-daily-blog-agent.md)
- [Venus: the autonomous social agent](venus-social-agent.md)

New agents are added to this page and get their own case study.

## Adding an agent
Write its mandate first. Create its definition, state files and notes file to the standard above. Add it to the org chart. Run it once by hand and review the output before putting it on a schedule. Log the decision.
