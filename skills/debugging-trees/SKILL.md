---
name: debugging-trees
description: Use this on bug hunts and ambiguous problems. Reconstruct the hypothesis tree and watch how the mental model changes.
---

# Debugging Trees

## What to Extract

For each debugging episode, score:

- how many candidate explanations were generated before the first fix
- anchoring: was the first plausible explanation also the last one tested
- discriminating evidence: tests designed to separate hypotheses, or only
  tests confirming the favorite
- cheapest-first ordering: were cheap probes run before expensive ones
- model updates: did contradicting evidence change the working theory
- symptom patches: fixes applied without causal understanding
- search shape: systematic narrowing or random walk

## Representative Trees

Reconstruct three to five full trees. For each:

1. entry observation
2. branches considered, in order
3. dead ends and what closed them
4. the update moment - what evidence finally moved the mental model
5. distance between root cause and where the search started

## Mental Model Timeline

Across one long debugging session, snapshot the working theory after each
major turn. The interesting signal is the jump size: incremental updates
versus wholesale replacement versus stubborn survival.

## When It Backfires

- Hindsight bias. With today's knowledge every tree looks dumb somewhere.
  Judge branch choices against available evidence at that moment.
- Counting the model's hypotheses as the subject's. In co-debugging,
  attribute every branch (episode-method).
- Cherry-picking disaster sessions. Include routine debugs; they show the
  default tree.

## One-Line Memory

Draw the tree. Count the branches. Watch the updates.
