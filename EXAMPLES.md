# A Full Audit, End to End (Demo)

Everything below comes from a FICTIONAL operator, built to show the exact
formats a real audit produces. The numbers are invented. The standards are
not: every claim carries evidence, frequency, counterevidence, confidence,
and an action.

## Input

```text
CORPUS
  window         6 months
  platforms      Claude Code, Codex CLI, Cursor
  sessions       1,847 parsed   (31 discovered-but-unreadable, reported)
  prompts        12,404
  projects       23
  coverage       HIGH for Claude Code, MEDIUM for Codex (logs rotated),
                 LOW for ChatGPT web (not exportable) - excluded, noted
```

## Output: five findings

### 🔍 "You don't have a debugging problem. You have a second-attempt problem."

Across 47 debugging sessions, the first attempt usually started from a
clear hypothesis. After attempt #1 failed, scope got widened instead in
61% of cases. Those sessions took 2.4x more iterations to close.

EVIDENCE: 47 episodes scored on second-move taxonomy; 29 widened scope.
COUNTEREVIDENCE: 9 sessions switched tools productively - all involved
environment issues, not logic bugs.
ALTERNATIVE EXPLANATION: hard bugs legitimately need wider search;
partially true - widening still lost to hypothesis-splitting on matched
difficulty pairs.
CONFIDENCE: HIGH
ACTION: after attempt #2 fails, force three competing hypotheses before
editing anything again.

### ⚡ "You say you prefer simple solutions. Your behavior says otherwise."

38 requests to "keep it simple." In 24 of those tasks, scope expanded
after the first implementation failed. Complexity entered during recovery,
never initial design.

COUNTEREVIDENCE: 14 tasks stayed simple - all had written success criteria
before starting.
CONFIDENCE: MEDIUM-HIGH
ACTION: no task starts recovery without restating the original scope line.

### 🤖 "Claude makes you think. Codex makes you move."

Claude sessions contained more research and option generation. Codex
sessions reached implementation fastest - but architecture-level work done
in Codex was reopened twice as often within 60 days.

ME x MODEL MATRIX (excerpt):

| Task type | Best completion | Least rework | Notes |
|---|---|---|---|
| architecture | Claude | Claude | Codex reopen rate 2.1x |
| implementation | tie | Codex | fewest correction loops |
| debugging | tie | tie | depends who forms hypotheses first |

CONFIDENCE: HIGH (implementation cells), MEDIUM (architecture, n=19)
ACTION: route architecture through Claude; stop switching mid-task.

### 🔁 "You've learned this lesson 11 times."

The same API-boundary mistake, corrected across 7 months, 4 projects,
3 different models. Verdict: KNOWN BUT NOT APPLIED - explained fluently,
violated anyway.

ACTION: mechanical guard, not memory. One lint rule would have caught
all 11 instances.

### ⚠️ "Verification doesn't degrade evenly. It disappears exactly when deadlines appear."

In 9 of 11 deadline-pressure deployments, no check exists between final AI
output and ship. Confidence language stays identical to relaxed sessions -
tone did not drop, checking did.

COUNTEREVIDENCE: both payments-related changes kept full checks. Risk
sensitivity exists but is scoped to money paths.
CONFIDENCE: HIGH
LIMITS: checks may have happened outside recorded sessions; cannot be
ruled out.
ACTION: pre-ship hook blocking untested-module deploys. Memory-based
corrections already failed twice here.

## What the full report adds

HOW YOU ACTUALLY WORK - one page
YOUR 10 SURPRISING PATTERNS
BELIEF VS BEHAVIOR table
DECISION OPERATING SYSTEM
STRENGTH -> SHADOW PAIRS
RECURRING FAILURE LOOPS, ranked
WHAT YOU ACTUALLY LEARN
DELEGATION FRONTIER - delegate / verify / collaborate / keep human-led
ME x MODEL MATRIX
WHERE AI MAKES YOU BETTER / WORSE / ONLY FEELS EASIER
HIDDEN BOTTLENECKS
PERSONAL OPERATING MANUAL - ~10 WHEN/DO/BECAUSE rules
EARLY-WARNING SIGNALS
THREE CHANGES ONLY
LEARNING ROADMAP
WHAT THESE DATA CANNOT KNOW

## What to notice

- Every claim has counts, date ranges, and platforms attached.
- Counterevidence was hunted on purpose, not stumbled on.
- Model behavior and human behavior are separated throughout.
- Fixes are mechanical where memory already failed - that call came from
  the learning-tracker verdicts, not intuition.
- The report names what the data cannot show. Twice.
