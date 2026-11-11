> **Experimental. We are just trying this.** [Disclaimer](../DISCLAIMER.md) · Counts only. Pre-run 1. Not Wednesday. Not Tuesday.

# Failed

Pre-run 1 did not complete. It is marked failed.

- Time of this note: 2026-11-11T07:20:00Z.
- What failed: the desk and Mini reset or restarted during the pre-run. After that reset, nothing was armed for send.
- The start had passed, and Tuesday's runner was down. [logs/PRE-RUN-OPEN.md](PRE-RUN-OPEN.md) is on origin from 2026-11-10T23:05:11Z, commit dd38ec9 (`PRE_RUN_OPEN 2026-11-10T23:05:11Z`). Mini published [logs/MINI-ARMED.md](MINI-ARMED.md) at 2026-11-10T23:15:29Z, commit 0dc3c0c (`MINI_ARMED 2026-11-10T23:15:28Z`).
- No hash file was published. No desk, Mini, or bot count file was published. There is no HOLD-1, HOLD-2, HOLD-3, HOLD-4, or RETURN on origin.
- The bot waiter was still polling at 2026-11-11T07:16:04+01:00 with `PRE-RUN-OPEN` present and desk HOLD-3 absent. The operator stopped that waiter at 2026-11-11T07:16:33+01:00. The bot did not send. [BOT-HALT.md](BOT-HALT.md) records that stop.
- At 2026-11-11T07:17:58+01:00 the desk was reachable and had last booted at 2026-11-11T01:31:08+01:00. No kaspad, miner, or sender process was running on it. Mini was not reachable, so its processes could not be read.
- This is a rehearsal miss, not Wednesday's count and not a number for Pulse. Wednesday's repo and Tuesday's repo were not edited.
- The next attempt, if opened, is a new repo, `tn10-storm-2026-11-11-prerun-2`, and it starts from [locks/LOCKED.md](../locks/LOCKED.md). This repo's pastes are not rewritten.
