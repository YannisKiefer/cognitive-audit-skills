# Promotion Kit

Everything needed to launch cognitive-audit-skills. Positioning is fixed;
wording can be adapted.

## Core positioning

> Your AI coding history is a dataset about how you work.
> Nobody has ever read it all together. An agent can.

The product is the experience: point an agent at months of Codex, Claude,
Cursor sessions, get back patterns about yourself that no single chat
could show. The 18 skills are the method, not the pitch.

## Ten headline options

1. Your AI history is a dataset about how you work. Nobody has ever run
   the analysis.
2. One chat shows what you did. Ten thousand show how you operate.
3. You've generated years of evidence about your own thinking. Time to
   read it.
4. Every mistake you keep making lives somewhere in your logs. Find them
   all at once.
5. Stop asking AI to analyze you from one conversation. You have
   thousands.
6. An audit of you, written from evidence you generated without knowing.
7. The most honest profile of you as a developer was never written.
   It's in your logs.
8. What would an agent find, reading every session you've ever had?
9. You can't see your patterns from inside a chat. Across 500 of them,
   they're obvious.
10. Your AI watched you make 10,000 decisions. Make it tell you what it
    saw.

## Five GitHub About descriptions

1. Point an AI at your entire Claude, Codex & Cursor history - get an
   evidence-backed audit of how you actually work. Not vibes: counts,
   dates, counterexamples.
2. One chat shows what you did. 10,000 chats show how you operate. Agent
   skills that investigate your entire coding history.
3. Your AI history is a dataset about how you work. These 18 skills make
   an agent read all of it and report the patterns.
4. An AI investigates your own coding sessions and finds behavioral
   patterns invisible from inside any single chat.
5. Evidence over horoscopes: turn thousands of real sessions into a
   confidence-rated audit of how you think, debug, and build.

Current applied: #1.

## First-audit prompt (canonical)

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

## Social preview (1280x640)

Dark background (#0d1117), red accent (#f85149).

Line 1 (huge, bold): YOUR AI HISTORY KNOWS HOW YOU WORK.
Line 2 (medium): Now let an agent prove it.
Line 3 (small, mono): Claude / Codex / Cursor / OpenCode / Kimi / Grok
Chips along the bottom: `10,000 prompts` `12 months` `6 models`
`confidence-rated`

Rule: never claim "AI understands you better than yourself." Claim:
patterns across thousands of decisions, with receipts.

## Demo structure (for screenshots or video)

1. Show the corpus inventory first - raw scale sells: platforms, session
   counts, coverage table.
2. Then exactly three finding cards max. Full cards, not summaries -
   counterevidence and confidence are the differentiators.
3. Close on the belief-vs-behavior table; it screenshots well and stings
   appropriately.
4. End on "WHAT THESE DATA CANNOT KNOW" - the honesty section closes
   skeptics.
5. Blur/redact anything real. Fictional demo lives in EXAMPLES.md; real
   runs must be anonymized before publishing anywhere.

## X launch post

I have ~2 years of Claude + Codex history. Thousands of real decisions.
Never once looked at them together.

So I built 18 agent skills that do it for me:

- discover every local session store itself
- rebuild actual work episodes across models
- hunt counterexamples on purpose
- rate every finding high/medium/low confidence

First full run told me I'd "learned" the same lesson 11 times across
4 projects. It suggested a lint rule instead of memory. Correct call.

Not a personality quiz. No MBTI, no diagnoses. Just what I repeatedly did,
what happened next, and whether it kept happening.

Repo: https://github.com/YannisKiefer/cognitive-audit-skills

## Hacker News (Show HN)

Title: Show HN: Let an AI investigate your entire coding history

Body:

I kept noticing that individual AI chats mislead me about my own habits.
A single session can justify almost any story about how I work. The
pattern only showed up when I compared dozens of similar sessions - and
nobody manually compares 500 of their own conversations.

This repo is a pack of 18 agent skills (plain markdown, works with Claude
Code, opencode, Cursor, Codex CLI, anything that reads SKILL.md files)
that runs a longitudinal behavioral audit on your own machine:

1. discovers accessible session stores across tools (Codex, Claude Code,
   Cursor, OpenCode, Kimi, Grok, ChatGPT exports, git) and reports honest
   coverage - including what it could not parse
2. reconstructs work episodes rather than treating messages as data points
3. separates human behavior from model behavior - if the model proposed
   the bad architecture, that is not evidence you prefer bad architecture
4. requires repeated evidence across tasks/months/models before calling
   something a pattern, hunts counterexamples deliberately, and assigns
   confidence ratings
5. ends with a fixed-format report: dominant work loop, ten surprising
   patterns, belief-vs-behavior table, failure loops ranked by cost,
   which-model-for-which-task matrix, three changes with highest expected
   payoff

Deliberate design limits: it is not a personality tool - no MBTI, no
diagnoses, no clinical territory. Secrets are redacted and analysis stays
local. And retrospective analysis finds suspects, not verdicts, so the
last skill converts low-confidence claims into falsifiable predictions
your next sessions can settle.

Methodology borrows from aviation incident analysis, diagnostic error
research, and intelligence analysis doctrine; SOURCES.md cites the
peer-reviewed grounding (calibration research, programmer cognition,
automation bias, human-AI collaboration studies) separately from emerging
preprints.

Repo: https://github.com/YannisKiefer/cognitive-audit-skills

Interested in feedback on two things: whether the evidence bar (roughly 3
tasks x 3 months x 3 contexts per pattern) is right, and whether the
report format lands or should be more configurable.

## Reddit short version

Point an AI at your entire Claude/Codex/Cursor history and it will find
things about how you work that you genuinely cannot see from inside any
single chat. I built 18 open-source agent skills that do exactly this:
discover all your local session stores, rebuild real work episodes,
separate your behavior from the model's behavior, then demand repeated
evidence + counterexamples before reporting a pattern. Output is a report
with your top 10 surprising patterns, a belief-vs-behavior table, failure
loops ranked by cost, and a which-model-for-which-task matrix built from
your outcomes, not benchmarks. Explicitly not a personality quiz - no
MBTI/diagnosis stuff, secrets get redacted, everything runs locally.
MIT: repo link. The demo example in EXAMPLES.md shows the exact input/
output format.

## Channel notes

- X: lead with the personal number ("11 times"), not the feature list.
- HN: lead with the epistemics; HN punishes hype and rewards stated
  limits.
- Reddit: casual, first person, name the sub-appropriate angle
  (r/ClaudeAI: workflow; r/LocalLLaMA: local-only privacy).
