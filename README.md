<div align="center">

<img src="assets/banner.jpg?v=5" alt="the-ai-diary" width="100%"/>

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)
![Skills](https://img.shields.io/badge/skills-18-blue)
[![Format](https://img.shields.io/badge/format-SKILL.md-green)](https://github.com/anthropics/skills)

</div>

---

# Your AI has been keeping a diary about you.

Every prompt. Every bug. Every 2am "why won't this build".
Every time you typed "keep it simple" and then did the opposite.

Months of it. Thousands of sessions. Sitting on your disk right now,
across Claude, Codex, Cursor, and everything else you've used.

You will never read all of that. No human would.

**But an AI can.** And when it does, it comes back with stuff like this:

---

> ### 🔍 "You're a great debugger right up until the first failure. Then you panic."
>
> 47 debugging sessions. First attempt: usually sharp. After it fails?
> You ditch the hypothesis and start rewriting huge chunks - 61% of the
> time. Those sessions took 2.4x longer to close.
>
> **Fix:** after attempt #2 dies, write three competing theories before
> touching anything.

> ### 🔁 "You've 'learned' the same lesson 11 times."
>
> Same mistake. Spread over 7 months, 4 projects, 3 different models.
> You explained it perfectly every time. Then did it again.
>
> **Fix:** stop trusting memory. One lint rule catches all 11.

> ### 🤖 "Claude makes you think. Codex makes you move. You keep using them backwards."
>
> Architecture done in Codex got reopened twice as often within 60 days.
> Implementation done in Claude bought you nothing but slowness.
> Your own data already picked the winning split. You just never saw it.

> ### ⚡ "You say deadlines focus you. Deadlines make you ship untested code."
>
> 9 of 11 deploys under deadline pressure: zero checks between the AI's
> final answer and production. Your words stayed confident. Your
> behavior didn't.

*Example output - fictional operator, real format.*

---

## Now picture it running on YOUR history.

Nobody configures anything. You don't upload anything.

The agent goes looking through your machine itself. Finds every session
store, every log, every repo. Reads thousands of decisions you barely
remember making. Connects sessions you thought were unrelated. Counts
everything.

Then it tells you the patterns you've been living inside without seeing:

- the mistakes you keep making and quietly re-googling
- the lessons you "learned" that changed absolutely nothing
- what happens to your quality the exact moment you get impatient
- which model earns its place and which silently burns your hours
- what you claim to care about vs. what your logs prove you do
- where your time actually goes (rarely where you think)

You can't see any of this from inside a single chat. That's the point.
One conversation is an anecdote. Ten thousand are a mirror.

---

## How it works

```text
already on your disk:
    every Codex session
    every Claude chat
    every Cursor session
    every git commit
            |
            v
  one agent finds ALL of it itself
            |
            v
  reads it, connects it, counts everything
            |
            v
  kills every pattern it can't defend with evidence
            |
            v
  tells you what survived
```

Not what you said once. What you kept doing.

---

## Run it on yourself tonight

```bash
npx skills add YannisKiefer/the-ai-diary
```

Then paste this into your agent and walk away:

```text
Run a full cognitive audit on my own history.

Discover every accessible source: Codex, Claude Code, OpenCode, Kimi,
Grok, ChatGPT, git history - wherever sessions hide locally. Inventory
what exists, then reconstruct my work episodes across all of it. Separate
my behavior from the models' behavior everywhere. Find 10 patterns I
probably can't see myself. Require repeated evidence across tasks and
months. Hunt counterexamples on purpose. Rate each finding HIGH / MEDIUM /
LOW confidence and say what the data cannot show. Start with audit-router.
Redact any secrets. End with the 3 changes that have the highest expected
payoff.
```

## What comes out

```text
HOW YOU ACTUALLY WORK           <- one page, no fluff
YOUR 10 SURPRISING PATTERNS     <- each with proof AND counterevidence
BELIEF VS BEHAVIOR              <- the table that hurts
YOUR FAILURE LOOPS              <- ranked by what they cost you
WHAT YOU KEEP RE-LEARNING       <- the 11-times list
WHERE AI MAKES YOU BETTER
WHERE AI MAKES YOU WORSE        <- yes, it happens to everyone
WHICH MODEL FOR WHICH WORK      <- your data, not benchmarks
YOUR HIDDEN BOTTLENECKS         <- almost never coding speed
PERSONAL OPERATING MANUAL       <- ~10 WHEN / DO / BECAUSE rules
3 CHANGES WITH THE BIGGEST PAYOFF
```

Full demo run with input/output numbers: [EXAMPLES.md](EXAMPLES.md)

---

## Isn't this just cold reading?

Fair question. Here's the difference between this and pasting one chat
into ChatGPT and asking "analyze me":

| "analyze me" | cognitive audit |
|---|---|
| one conversation | every conversation you've ever had |
| "you seem ambitious" | "you widen scope after failure 61% of the time" |
| can't be wrong | counterevidence hunted on purpose |
| vibes | counts, dates, platforms |
| nothing changes Monday | three specific changes to try |

Weak claims get labeled weak. Patterns only survive if they show up
across tasks, months, and different models. And the report ends with a
section listing everything the data *cannot* tell you.

## Not therapy, promise

No MBTI. No diagnoses. No "you're ambitious and curious." Just what you
did, what happened next, and whether it keeps happening. Secrets get
redacted. Analysis runs locally - your history never leaves your machine.

## Under the hood

18 specialist skills do the digging - one finds your session stores, one
separates your behavior from the model's, one tracks repeated lessons,
one builds the model comparison, one hunts blindspots, one writes the
final report. Start at [audit-router](skills/audit-router/), or meet the
whole crew below.

| Lens | The question it answers |
|---|---|
| [audit-router](skills/audit-router/) | Where does the audit go next? |
| [source-discovery](skills/source-discovery/) | Where is your history hiding? |
| [evidence-hygiene](skills/evidence-hygiene/) | How do secrets stay out of the report? |
| [episode-method](skills/episode-method/) | What did YOU decide vs what did the model do? |
| [cognitive-loop-map](skills/cognitive-loop-map/) | How do you go from idea to done? |
| [framing-planning](skills/framing-planning/) | Plan enough - or forever? |
| [calibration-audit](skills/calibration-audit/) | When were you confident and wrong? |
| [debugging-trees](skills/debugging-trees/) | What does your debugging really look like? |
| [failure-loops](skills/failure-loops/) | What does your second move cost you? |
| [bias-candidates](skills/bias-candidates/) | Fooling yourself the same way, repeatedly? |
| [collaboration-audit](skills/collaboration-audit/) | Where does understanding leak? |
| [learning-tracker](skills/learning-tracker/) | What keeps coming back? |
| [attention-ledger](skills/attention-ledger/) | Where does the time actually go? |
| [model-matrix](skills/model-matrix/) | Which model wins, at what, in YOUR data? |
| [contradiction-finder](skills/contradiction-finder/) | Where do words and behavior disagree? |
| [blindspot-miner](skills/blindspot-miner/) | What's invisible from inside every single chat? |
| [report-writer](skills/report-writer/) | How does it become one readable report? |
| [prospective-kit](skills/prospective-kit/) | Which questions can next month settle? |

Method: [METHOD.md](METHOD.md) · Research grounding:
[SOURCES.md](SOURCES.md) · Contributing: [CONTRIBUTING.md](CONTRIBUTING.md)

## License

MIT. Fork it, ship it, run it on yourself.

<div align="center">
<sub>Built by <a href="https://github.com/YannisKiefer">Yannis Kiefer</a></sub>
</div>
