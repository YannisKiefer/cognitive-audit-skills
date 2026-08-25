---
name: evidence-hygiene
description: Use this whenever the corpus might contain secrets, customer data, or anything private. Protect it while analyzing it.
---

# Evidence Hygiene

## The Big Idea

You are reading someone's unlocked desk drawers. Session corpora routinely
contain API keys, credentials, customer records, proprietary code, and
production data. The audit's job is insight, not exposure.

## The Rules

1. Run a secrets pass before deep analysis. Scan for tokens, keys,
   passwords, connection strings, customer identifiers. Flag, then avoid.
2. Derive, don't duplicate. Analyze locally. Store derived observations,
   not bulk copies of raw conversations.
3. Redact quotes. Show the shape of a value, never the value:
   `sk-...REDACTED`, `postgres://user:***@host`. Keep enough structure to
   stay verifiable.
4. Raw secrets never appear in any report, note, summary, or log line.
5. Private client and store artifacts stay out of shared repos and product
   code. Anonymize examples unless the owner explicitly says otherwise.
6. Prefer local analysis over uploading the corpus anywhere.

## The Redaction Test

Before quoting evidence, ask:

> Would I be comfortable if this quote were pasted into a public issue?

If no, redact values, keep the reasoning visible.

## When It Backfires

Over-redaction destroys analytic value. A quote stripped of every noun
proves nothing. Fix: redact identifiers and secrets, keep logic, numbers,
and decisions intact.

## One-Line Memory

Derived observations travel. Raw secrets never.
