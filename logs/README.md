> **Experimental. We are just trying this.** [Disclaimer](../DISCLAIMER.md) · Counts only. Pre-run 1.

# Logs

| File | Who writes it | When |
|---|---|---|
| PRE-RUN-OPEN.md | the desk | at or after 23:00 CET (22:00 UTC) on 10 Nov 2026, once Tuesday's runner is down, before the first family submit. One line: `PRE_RUN_OPEN` and a UTC timestamp. Absent while the gate holds |
| MINI-ARMED.md | Mini | after `PRE-RUN-OPEN` is on origin. One line: `MINI_ARMED` and a UTC timestamp |
| FIXES.md | the desk | each repair. UTC time, what failed, what changed, why |
| METHOD.md | the desk | when RETURN is on origin, met or `NOT MET` |
| BOT-HALT.md | the operator | one line, any time, to stop the bot. Absent until the operator writes it |

`PRE-RUN-OPEN` is not a send. A paste before 23:00 CET (22:00 UTC) on 10 Nov 2026 does not write it. A paste while Tuesday's runner is up does not write it.

METHOD.md leads with accepted hops per cohort and payment accepts per target. It says whether the result was decent or short of decent, as [README.md](../README.md) defines those words. If the rates were one rate, or the coins were not one size, or the cohorts did not share one node set, it says so and does not call the fee the whole cause. Then the misses, the fixes, and the On origin time of each count file. A fee estimate is not a row.

A worked fix is also appended to [locks/LOCKED.md](../locks/LOCKED.md). This file does not rewrite a paste.
