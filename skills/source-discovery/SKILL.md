---
name: source-discovery
description: Use this to inventory every accessible history of human-AI work before analyzing anything. Discover paths; never assume them; measure coverage honestly.
---

# Source Discovery

## The Big Idea

An audit is only as good as its denominator.

Claiming "you do X in 60% of sessions" means nothing until you know how many
sessions exist, which platforms they came from, and how many you could
actually parse. Measure the denominator first or say nothing at all.

## The Sweep

Discover, don't assume. Paths drift between machines, versions, and apps.

1. List candidate platform homes under the user's home directory, config
   directories, app storage locations, and project folders.
2. Ask the user which platforms they used. Local files confirm or refute.
3. Include git history, task boards, agent logs, transcripts, prompt
   histories, and tool-call logs wherever accessible.
4. For each source found: record format, date range, volume, parse rate.

Typical platforms worth checking: Codex, Claude / Claude Code, OpenCode,
Kimi Code, Grok, other coding agents installed locally, ChatGPT coding
sessions where accessible, git repositories.

## The Coverage Report

Report exactly, for every platform:

- platform name
- accessible date range
- number of sessions
- number of user messages / prompts
- amount successfully parsed
- missing or corrupted data
- confidence in coverage

A platform with no accessible sessions is reported as "not available."
It is never silently skipped and never counted as analyzed.

## When It Backfires

- Assuming a path exists without listing it. Check.
- Counting sessions that were never opened or parsed.
- Treating one platform's absence as proof the user never used it.
- Burning the whole session on inventory. Good enough coverage beats
  perfect coverage; start analysis when the big platforms are mapped.

## One-Line Memory

Measure the denominator or say nothing.
