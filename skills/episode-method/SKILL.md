---
name: episode-method
description: Use this before interpreting anything in the corpus. Attribute behavior correctly, then rebuild work episodes as the unit of analysis.
---

# Episode Method

## Attribution First

You are analyzing human + model interactions. Never attribute the model's
behavior to the human.

Classify every observed action:

| Class | Meaning |
|---|---|
| USER INITIATED | The human asked, decided, or drove it |
| MODEL SUGGESTED | The model proposed it, human engaged |
| MODEL CAUSED | Model output produced the result |
| SYSTEM CONSTRAINT | Tooling, permissions, or environment forced it |
| UNKNOWN | Cannot tell - leave unknown, do not guess |

Worked examples of the trap:

- The model proposes complex architecture and the human discusses it. That
  is not evidence the human prefers complexity.
- The model repeatedly misunderstands a request. That is not automatically
  evidence the human communicates poorly.
- One agent needs more explicit prompting than another. Normalize for the
  agent before comparing humans' prompts across them.

Analyze within each model AND across models.

## Episodes, Not Messages

Individual messages are noise. The unit of analysis is the work episode.

An episode has up to ten stages: initial intention, problem framing,
research, planning, execution, failures, corrections, verification,
completion, later regression or reversal.

Follow tasks across multiple sessions where possible. The meaningful unit
is DECISION -> ACTION -> RESULT -> UPDATE.

## Extraction Schema

For each meaningful episode capture, when available: platform/model,
timestamp, project, task type, intended outcome, complexity, initial
framing, context supplied, success criteria set, planning performed,
research performed, hypotheses considered, implementation started, major
iterations, failures, corrections, model switches, tools used, validation,
tests, shipped or not, later rework, later reversal, human correction
required, repeated known mistake, lesson captured, lesson reused later.

Missing fields stay missing. Do not create false precision.

## One-Line Memory

Attribute first. Episodes second. Messages last.
