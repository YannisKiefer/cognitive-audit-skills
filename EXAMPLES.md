# Example Findings

What finished output looks like. The operator below is fictional; the
formats are the standard.

## A Finding That Survives

> **FINDING:** Under deadline pressure, verification collapses to zero
> while confidence language stays constant.
>
> **EVIDENCE:** 11 episodes across 3 projects where a stated deadline
> preceded deployment. In 9 of 11, no test or manual check appears between
> final AI output and ship. Confidence phrasing in messages is unchanged
> from low-pressure sessions.
>
> **FREQUENCY / RANGE / PLATFORMS:** 11 of 11 eligible episodes,
> Jan-Aug, Codex and Claude Code.
>
> **COUNTEREVIDENCE:** 2 episodes with checks preserved under deadline -
> both were payments-related, suggesting risk-sensitivity exists but is
> scoped to money paths only.
>
> **ALTERNATIVE EXPLANATION:** Checks may have happened outside recorded
> sessions. Cannot be ruled out; noted in limits.
>
> **CONFIDENCE:** HIGH
>
> **CONSEQUENCE + FIX:** Non-critical paths ship unverified under time
> pressure. Fix is mechanical: pre-ship hook that blocks deploys when the
> diff touches untested modules. Memory-based fixes already failed here -
> this exact lesson was corrected twice before without sticking.
>
> Would the subject nod immediately? No - they report being "pretty
> disciplined about testing."

## A Horoscope Line That Doesn't

> "You are a driven builder who learns fast and cares about quality."

True for nearly every developer alive. Visible inside any single session.
Zero intervention value. This fails the filter and does not enter the
report.

## One Belief vs Behavior Row

| What I appear to believe | What behavior shows | Evidence | Consequence |
|---|---|---|---|
| Model switching unblocks stuck tasks | Frustration-triggered switches restart the same loop 4 of 6 times | Switch forensics, Mar-Jul, 3 models | A written blocker checklist beats a second opinion |

## One Failure Loop Card

TRIGGER: first fix attempt fails
-> RESPONSE: re-prompt with more specificity, same theory intact
-> SHORT-TERM BENEFIT: feels like progress, sometimes lands
-> LONG-TERM COST: 2.4x longer failure loops on architecture bugs
-> INTERRUPTION: after attempt two fails, write down two competing
hypotheses before touching anything

## One Early-Warning Signal

"If you have re-prompted the same error twice with no new information
gathered, stop and run one discriminating test."

## What to Notice

- Every claim carries counts, ranges, platforms, counterevidence.
- Attribution is explicit: model behavior never became human behavior.
- The fix is tooling, not willpower - because the tracker showed
  memory-based corrections had already failed twice.
