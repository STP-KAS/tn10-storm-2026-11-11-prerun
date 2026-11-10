> **Experimental. We are just trying this.** [Disclaimer](../DISCLAIMER.md) · This page does not start a machine.
>
> Lines here are locked for the next pre-run. This pre-run does not reopen them. Wednesday's plan is not edited from this page.

# Locked

## Locked before pre-run 1

These came from the Wednesday review, through round 4, and this pre-run keeps them.

- The desk keeps every public node it used in HOLD-3. It does not drop one to free it for the bot.
- The bot sends only on a synced public node outside that set, one process, and only in the HOLD-4 minute. No free node means `NO SEND` and `no-free-node`. The bot has no local node.
- The HOLD-4 minute is the first whole UTC minute whose start is at least 3 minutes after the HOLD-3 file's On origin time. Both sides read that time from origin. An unsynced minute is still that minute. The run does not open a later one.
- Mini publishes HOLD-4 when the bot file is on origin, or `logs/BOT-HALT.md` is on origin, or the desk's HOLD-4 file has been on origin for 10 minutes. `TWO SENDERS` only when the bot file is on origin and is not `NO SEND`. Mini does not republish.
- Families 1–13 and families 14–16 use the same family-sender nodes. Fees stay 100, 200, and 150 sompi per gram. A priority quote is not read. A fee estimate is not read.
- Mini is the only chain counter. Mini does not send. The bot stays out of HOLD-1, HOLD-2, HOLD-3, and RETURN.
- The abort line stays 2,500 coins and 18,000 usable tKAS. The desk node process is not stopped by this pre-run.
- This repo does not edit Tuesday's repo and does not edit Wednesday's repo.

## Locked during this pre-run

Nothing yet. When a fix works, append it here before the next pre-run is written.

One block per fix:

```
- UTC time.
- What failed.
- What was changed.
- Why that change stays.
```

The go files in this repo stay as they were at the paste. The next repo copies this page and bakes the new lines into its own pastes.
