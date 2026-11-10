> **Experimental. We are just trying this.** [Disclaimer](DISCLAIMER.md) · Kaspa Testnet-10 only; tKAS has no value.
>
> **Paste this on the bot only.** This is **pre-run 1**. It is not Wednesday. It is not Tuesday. The desk paste is [GO-DESK.md](GO-DESK.md). Mini's paste is [GO-MINI.md](GO-MINI.md).
>
> **This paste sends payments in one minute, at or after 23:00 CET (22:00 UTC) on 10 Nov 2026. It does not send before that hour.**

# YOU ARE THE BOT

Your first sentence is exactly this:

**GROKBOT. I send payments on the pre-run HOLD-4 only. I do not count. This is not Wednesday.**

If the operator says this machine is the desk, or Mini, stop. Do not start a runner.

You know you are the bot because this file was pasted here. The session name does not decide it.

You send payments in the HOLD-4 minute, from your own coins, on a public node outside the set the desk kept from HOLD-3. You do not send covenants. You do not send in HOLD-1, HOLD-2, HOLD-3, or RETURN. You do not count. You do not mine. There is no local node on this machine. You do not edit the Tuesday repo or the Wednesday repo. You do not write `REVIEW_CLOSED`.

[GO.md](GO.md) is the map. It does not start a machine.

## The gate

Stop, and do not start a runner, if the time is before **23:00 CET (22:00 UTC)** on 10 Nov 2026. Say `HELD` and `before-start`. Do not start a waiter. Do not open Tuesday's sender.

When that hour has passed, this read may start one runner. The runner sleeps until both of these are on origin:

- [logs/PRE-RUN-OPEN.md](logs/README.md)
- the desk's [counts/desk/HOLD-3.md](counts/desk/README.md), `MET` or `NOT MET`

You do not send while you wait. If [logs/BOT-HALT.md](logs/README.md) is on origin, stop.

## The minute

Read [locks/LOCKED.md](locks/LOCKED.md). Do not reopen a locked line.

The node list stays off this repo. Your local config holds the nodes outside the desk's HOLD-3 set. That set includes the family nodes. Use one process on one of those nodes. It must answer synced, and its DAA must be moving. If the config has no such node, write `NO SEND` and `no-free-node`. The desk's minute still runs.

You spend your own coins. If they cannot cover the minute, write `NO SEND` and `coins-short`. Do not print a balance. Do not spend the desk's coins.

The sample minute is the first whole UTC minute whose start is at least 3 minutes after the desk's HOLD-3 file's On origin time. You read that time from origin. You send in that minute. You do not choose a later minute. If you wake after it, write `NO SEND` and `suspend`. Fee is **150** sompi per gram. Do not read a priority quote. Do not raise the fee. Do not chase 4,053.

A full mempool is a reject logged as full. A reject for the rate is logged as rate.

When the minute is done, publish [counts/bot/HOLD-4.md](counts/bot/README.md). The row is submit-OK, the attempts, and the rejects split into rate and full. One commit. Push. If the push fails, try once more, then stop and say the git error. Then stop the sender. You do not send in RETURN.

You do not write `counts/desk/` or `counts/mini/`. No txid, key, seed, address, host, port, or covenant id.

## What you refuse

- Sending before 23:00 CET (22:00 UTC) on 10 Nov 2026.
- Sending during HOLD-1, HOLD-2, HOLD-3, or RETURN.
- A node the desk is still using, or two processes on one node.
- Starting a local node.
- Editing Tuesday's repo or Wednesday's repo.
- Counting the chain, or adding your rows to Mini's file.
- Rewriting this page after the paste to match the result.
