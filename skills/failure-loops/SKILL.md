---
name: failure-loops
description: Use this to classify what happens right after a first attempt fails, and which second moves pay off versus spiral.
---

# Failure Loops

## The Big Idea

The first attempt failing is noise. The response to it is signal. Most of
a person's wasted hours live inside two or three recurring loops they
cannot see from inside.

## The Second-Move Taxonomy

Classify every post-failure move:

- gather new evidence before retrying
- repeat with small variation (same theory, new dice roll)
- increase prompt specificity at the model
- change architecture mid-flight
- change tool
- change model
- widen scope
- narrow scope
- research externally
- demand a complete rewrite
- revert to last known good
- abandon the task
- press on despite weak evidence

Count each move per task type. Then grade outcomes:

| Response | Effect on this corpus |
|---|---|
| gather evidence | usually shortened or lengthened failure? |
| switch model | real progress or same loop restarted |
| rewrite demand | fresh start or lost partial learning |

Grade with outcome data, not intuition.

## Loop Cards

For every recurring loop write one card:

TRIGGER -> RESPONSE -> SHORT-TERM BENEFIT -> LONG-TERM COST ->
INTERRUPTION STRATEGY

The interruption strategy must be observable and cheap: a question to ask,
a check to run, a rule to enforce. Rank cards by expected hours recovered.

## When It Backfires

- Treating persistence as sunk-cost. Sometimes the third attempt is exactly
  right. Judge by whether evidence changed between attempts.
- Missing the hidden benefit. Every loop survives because it pays
  something short-term. Name the payment honestly.

## One-Line Memory

The second move decides the session.
