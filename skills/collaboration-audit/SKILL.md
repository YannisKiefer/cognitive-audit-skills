---
name: collaboration-audit
description: Use this to map the full human-AI working loop - prompts in, verification out, understanding kept or leaked.
---

# Collaboration Audit

## Lens 1: Inputs

Judge prompts by functional properties, never by grammar, brevity,
informality, or voice dictation:

- desired outcome present
- relevant context present
- constraints present
- examples present
- success criteria present
- authority boundaries present
- verification requested
- unnecessary instructions
- conflicting instructions

Find the highest-performing prompt patterns in this corpus - the ones
associated with fewer correction loops.

Then list instructions the subject retypes manually again and again.
Each one is a candidate repo context file, skill, test, or guardrail.
Memory is the wrong storage for repeated rules.

## Lens 2: Output Handling

After plausible AI output arrives, classify the response: inspect, test,
ask why, request sources, run a reproduction, compare alternatives,
implement immediately, ship immediately.

Measure verification depth against risk level. Hunt both directions:

- AI SOUNDED CORRECT but result was wrong - what check was skipped
- excessive verification burned hours on a reversible, cheap decision

The goal is calibrated checking, not maximum checking.

## Lens 3: Understanding Ledger

Map tasks onto delegation levels: autocomplete, implementer, researcher,
debugger, architect, decision adviser, autonomous operator.

Then locate:

- delegation that saved weeks
- delegation that manufactured rework
- where the subject stays intellectually involved and thrives
- where evaluation replaced understanding and cost them later
- concepts repeatedly re-explained in later sessions
- where AI visibly accelerated genuine learning
- where the underlying system became a black box

## One-Line Memory

Calibrated checking beats maximum checking.
