> **Experimental. We are just trying this.** [Disclaimer](../DISCLAIMER.md) · Counts only. Pre-run 1.

# Logs

| File | Who writes it | When |
|---|---|---|
| PRE-RUN-OPEN.md | the desk | when the Tuesday gate is open, before the first family submit. One line: `PRE_RUN_OPEN` and a UTC timestamp. Absent while the gate holds |
| MINI-ARMED.md | Mini | after `PRE-RUN-OPEN` is on origin. One line: `MINI_ARMED` and a UTC timestamp |
| FIXES.md | the desk | each repair. UTC time, what failed, what changed, why |
| METHOD.md | the desk | when RETURN is on origin, met or `NOT MET` |
| BOT-HALT.md | the operator | one line, any time, to stop the bot. Absent until the operator writes it |

`PRE-RUN-OPEN` is not a send. A paste before 2026-11-10T22:15:00Z does not write it.

METHOD.md leads with accepted hops per cohort and payment accepts per target. It says whether the result was decent or short of decent, as [README.md](../README.md) defines those words. Then the misses, the fixes, and the On origin time of each count file. A fee estimate is not a row.

A worked fix is also appended to [locks/LOCKED.md](../locks/LOCKED.md). This file does not rewrite a paste.
