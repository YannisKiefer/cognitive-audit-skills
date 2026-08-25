<div align="center">

<img src="assets/banner.svg" alt="cognitive-audit-skills" width="100%"/>

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)
![Skills](https://img.shields.io/badge/skills-18-blue)
[![Format](https://img.shields.io/badge/format-SKILL.md-green)](https://github.com/anthropics/skills)

</div>

---

# Your AI history is a dataset about how you work.

Every session you've had with Claude Code, Codex, Cursor, OpenCode, Kimi,
Grok, or ChatGPT is a record of a real decision. How you framed the
problem. What you tried first. What broke. What you did next.

One conversation shows what you did.

Ten thousand, read together, show **how you operate** - including things
you cannot see from inside any single chat. Which mistakes you repeat.
Which lessons never stick. Where your hours actually go. Which model makes
you better, and which quietly makes you worse.

Nobody manually reads 10,000 of their own prompts looking for patterns.
An agent can.

These 18 skills give it the method.

---

## What kind of findings? Like these.

> Example output from a demo audit. Fictional operator, realistic numbers.

### 🔍 "You don't have a debugging problem. You have a second-attempt problem."

Across 47 debugging sessions, the first attempt usually started from a
clear hypothesis. After it failed, you switched to broad rewrites in 61%
of cases. Those sessions took 2.4x more iterations to close.

**Pattern:** first failure → abandon hypothesis → widen scope
**Try:** after attempt #2 fails, force three competing hypotheses before editing again

### ⚡ "You say you prefer simple solutions. Your behavior says otherwise."

You asked to "keep it simple" 38 times. In 24 of those tasks, scope
expanded after the first implementation failed. The complexity entered
during recovery, not design.

### 🤖 "Claude makes you think. Codex makes you move."

Claude sessions held more research and option generation. Codex sessions
reached implementation faster - but architecture tasks done in Codex were
reopened twice as often.

**Your best split may be:** Claude for architecture, Codex for execution.

### 🔁 "You've learned this lesson 11 times."

The same API-boundary mistake, corrected across 7 months, 4 projects,
and 3 different models. The problem stopped being knowledge long ago.
That fix belongs in a lint rule, not in your memory.

Full demo audit with input/output numbers: [EXAMPLES.md](EXAMPLES.md)

---

## What would it find in yours?

- 🧠 Do you actually form hypotheses, or jump straight to code?
- 🔁 Which lessons have you "learned" more than once?
- 🎯 What do you believe you're good at - and what do outcomes say?
- 🤖 Which model genuinely produces fewer rework loops *for you*?
- ⚠️ Where does AI make you faster at shipping wrong answers?
- 🪞 Where do your stated priorities and your logged behavior disagree?
- ⏱️ How much of your time goes to product versus meta-work about work?
- 📚 Which mistakes vanish after one correction, and which return monthly?

You can answer any of these badly from memory. The corpus answers them
with counts, dates, and counterexamples.

---

## How it works

```text
your AI history
      |
      v
Claude + Codex + Cursor + OpenCode + Kimi + Grok + git + ...
      |
      v
agent discovers every accessible source itself
      |
      v
rebuilds real work episodes from the message noise
      |
      v
separates YOUR behavior from the MODEL'S behavior
      |
      v
compares decisions -> actions -> outcomes, across months
      |
      v
challenges every candidate pattern with counterexamples
      |
      v
shows you what survived, with confidence ratings
```

Not what you said once. What you repeatedly did.

---

## This is not an "analyze me" prompt

| Normal "analyze me" | This audit |
|---|---|
| one conversation | months of sessions, every platform |
| personality adjectives | observable behavior |
| vibes | counts, dates, ranges |
| cherry-picked moments | repeated patterns required |
| "you seem ambitious" | "after first failure you widen scope 61% of the time" |
| static description | specific intervention |
| nothing can disprove it | counterevidence hunted on purpose |

And it runs like an investigation, not a quiz. The agent discovers your
session stores itself, inventories what exists and what is unreadable,
reconstructs tasks that span multiple sessions, normalizes differences
between models, grades every claim HIGH/MEDIUM/LOW confidence, and ends
by telling you what the data *cannot* show.

---

## Run your first audit

```bash
npx skills add YannisKiefer/cognitive-audit-skills
```

Then paste this into your agent:

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

## What you get back

```text
HOW YOU ACTUALLY WORK            <- one page, plain language
YOUR 10 SURPRISING PATTERNS      <- each with evidence + counterevidence
BELIEF VS BEHAVIOR               <- the uncomfortable table
YOUR RECURRING FAILURE LOOPS     <- ranked by cost
WHAT YOU ACTUALLY LEARN          <- and what you keep re-learning
WHERE AI MAKES YOU BETTER
WHERE AI MAKES YOU WORSE
ME x MODEL MATRIX                <- which model for which work
YOUR HIDDEN BOTTLENECKS          <- rarely where you think
YOUR PERSONAL OPERATING MANUAL   <- ~10 WHEN/DO/BECAUSE rules
3 CHANGES WITH THE HIGHEST ROI
```

---

## Under the hood: 18 specialist lenses

| Lens | The question it answers |
|---|---|
| [audit-router](skills/audit-router/) | Where does the audit go next? |
| [source-discovery](skills/source-discovery/) | Where is your history hiding, and how much of it survives? |
| [evidence-hygiene](skills/evidence-hygiene/) | How do secrets stay out of the report? |
| [episode-method](skills/episode-method/) | What did *you* decide vs what did the model do? |
| [cognitive-loop-map](skills/cognitive-loop-map/) | How do you go from idea to done - and where does it break? |
| [framing-planning](skills/framing-planning/) | Do you frame problems well? Plan enough - or forever? |
| [calibration-audit](skills/calibration-audit/) | When were you confident and wrong? |
| [debugging-trees](skills/debugging-trees/) | What does your debugging actually look like, branch by branch? |
| [failure-loops](skills/failure-loops/) | What does your second move after failure cost you? |
| [bias-candidates](skills/bias-candidates/) | Are you fooling yourself the same way, repeatedly? |
| [collaboration-audit](skills/collaboration-audit/) | Prompts in, checks out - where does understanding leak? |
| [learning-tracker](skills/learning-tracker/) | What have you had to learn more than once? |
| [attention-ledger](skills/attention-ledger/) | What gets your time - and what actually pays off? |
| [model-matrix](skills/model-matrix/) | Which model wins, at which task, in *your* data? |
| [contradiction-finder](skills/contradiction-finder/) | Where do your words and your behavior disagree? |
| [blindspot-miner](skills/blindspot-miner/) | What's invisible from inside every single session? |
| [report-writer](skills/report-writer/) | How does all of it become one readable report? |
| [prospective-kit](skills/prospective-kit/) | Which open questions can your next 30 sessions settle? |

Start with [audit-router](skills/audit-router/). It routes everything else.

---

## This is not AI therapy

No MBTI. No IQ guesses. No diagnoses. No archetypes. No "you're ambitious
and curious."

It analyzes observable work behavior: what you did, what happened next,
whether it keeps happening. If the data can't support a claim, the report
says so in writing.

**Rules baked into every skill:**

1. Behavior over labels.
2. Never blame the human for the model's behavior.
3. Three tasks, three months, three contexts before a pattern exists.
4. Secrets never leave the corpus - redacted quotes, local analysis,
   derived observations only.
5. Surprising and actionable beats flattering.

---

## Why trust the method

The pipeline borrows from fields that investigate human performance for a
living: aviation incident analysis, diagnostic medicine, intelligence
analysis. Every finding must carry evidence, frequency, date range,
counterevidence, alternative explanations, and a confidence rating before
it reaches the report.

The research grounding is peer-reviewed and cited -
metacognition, calibration, programmer cognition, automation bias,
human-AI collaboration - see [SOURCES.md](SOURCES.md), with established
work separated from emerging preprints.

And one honest limit, stated up front: retrospective analysis finds
suspects, not verdicts. Confounders exist, offline behavior is invisible,
and selection bias toward recorded work is real. So the audit ends by
converting its weakest claims into falsifiable predictions your future
sessions can settle ([prospective-kit](skills/prospective-kit/)).

Method overview: [METHOD.md](METHOD.md)

## Contributing

New lenses welcome if they pass the filter:
**would this still be interesting if the subject already knew it?**
See [CONTRIBUTING.md](CONTRIBUTING.md).

## License

MIT. Fork it, ship it, run it on your own history.

<div align="center">
<sub>Built by <a href="https://github.com/YannisKiefer">Yannis Kiefer</a></sub>
</div>
