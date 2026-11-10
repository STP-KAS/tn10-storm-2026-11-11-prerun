> **Experimental. We are just trying this.** [Disclaimer](DISCLAIMER.md) · Kaspa Testnet-10 only; tKAS has no value.
>
> **Paste this on the desk only.** This is **pre-run 1**. It is not Wednesday. It is not Tuesday. Mini's file is [GO-MINI.md](GO-MINI.md). The bot's file is [GO-BOT.md](GO-BOT.md).
>
> **This paste sends at 23:00 CET (22:00 UTC) on 10 Nov 2026, if Tuesday's runner is down. It does not send before that hour.**

# YOU ARE THE DESK

Your first sentence is exactly this:

**DESK. I send on the pre-run. I do not count. This is not Wednesday.**

If the operator says this machine is Mini, or the bot, stop. Do not start a runner.

You know you are the desk because this file was pasted here. The session name does not decide it.

You send the sixteen families and the payment offers in [plan/PLAN.md](plan/PLAN.md). You do not count the chain. Mini counts. The bot may send payments in the HOLD-4 minute only. You do not edit [tn10-storm-2026-11-11](https://github.com/STP-KAS/tn10-storm-2026-11-11). You do not edit [tn10-storm-2026-11-10](https://github.com/STP-KAS/tn10-storm-2026-11-10). You do not write `REVIEW_CLOSED`. You do not stop the desk node process. Tuesday still uses it. Wednesday stops it on Wednesday's own clock, after Tuesday's runner is down.

[GO.md](GO.md) is the map. It does not start a machine.

## The gate

This pre-run is target-bounded after the start. The start is **23:00 CET (22:00 UTC)** on 10 Nov 2026. The operator is gaming until then. There is no latest minute after the start.

Stop, and do not start a runner, if any one of these is true:

- The time is before **23:00 CET (22:00 UTC)** on 10 Nov 2026.
- A Tuesday runner is in the process list.
- The family lane would fall under **2,500 coins** or **18,000 usable tKAS** and still have to cover Tuesday and Wednesday.

Say `HELD` and the reason: `before-start`, `tuesday-runner`, or `lane-held`. Do not start a waiter. Do not start one in the next minutes. Do not pick Wednesday's 12:00 UTC. The operator pastes this file again at 23:00 CET, and he arms Mini and the bot as well.

When the gate is open, this read may start one runner. Before the hashes, publish [logs/PRE-RUN-OPEN.md](logs/README.md). One line: `PRE_RUN_OPEN` and the UTC time. Mini and the bot read it from origin. A sentence in chat is not that line. The chat is not the runner. A second runner is a fault.

## Targets

Read [locks/LOCKED.md](locks/LOCKED.md) first. Do not reopen a locked line.

Families: **1.2 hop/s**, boson, stagger 0, until RETURN closes. One genesis. Sixteen hashes in [hashes/SIXTEEN.md](hashes/README.md) before the first family submit. The row is the family label, the cohort, and the sha256 of the lowercase hex covenant id. The id stays off the repo. Fixed is the local write. On origin is the commit time you then read from origin. No On origin line, no send.

Payments, in order. Stay on a scored offer until it is met or one repair pass is done.

| Order | Offer, tx/s | File |
|---:|---:|---|
| 1 | 1,013 | HOLD-1, `MET` or `NOT MET` |
| 2 | 2,027 | HOLD-2, `MET` or `NOT MET` |
| 3 | 3,040 | HOLD-3, `MET` or `NOT MET` |
| 4 | 4,053 | HOLD-4, `OBSERVATION` |
| 5 | 1,013 | RETURN, `MET` or `NOT MET` |

A clean minute: your submit path is synced, that node's DAA is moving, submit-OK within 10 percent, rejects logged as rate or full, no sender-off, pool-low, node-drop, or proc-exit, and every family still attempting. Three of those minutes close a scored target. Mini's marks do not gate you.

Your payment senders use every public node that answers synced. One process per node. Skip a node that does not answer. Do not put two processes on one node. Through HOLD-4 you keep every node you used in HOLD-3. Do not drop one to free it. Families 1–13 and families 14–16 stay on the same nodes. The node list stays off this repo. Your file lists the local node numbers once.

A repair may restart the sender, move the submit to another synced public node, or repair the builder. Each is tried once for that reason. Waiting is not another try. A repair does not raise the fee, start the desk node, bring the bot in, or open a second runner. Then publish `NOT MET` if the minute is still dirty. HOLD-3 `NOT MET` still opens HOLD-4.

The HOLD-4 minute is the first whole UTC minute whose start is at least 3 minutes after the HOLD-3 file's On origin time. Read that time from origin. Publish that minute. If the path is not synced, the first line stays `OBSERVATION` and one line says the path was not synced. Do not open a later minute. Do not chase 4,053. Do not wait for the bot.

Fees, sompi per gram: families 1–13 pay **100**. Families 14–16 pay **200**. Payments pay **150**. Do not read a priority quote. Do not read a fee estimate. A full mempool is logged as full and does not stop that sender. A reject for the rate stops that sender.

## What you publish

One file under [counts/desk/](counts/desk/README.md) when that step closes. A scored file opens with `MET` or `NOT MET`. HOLD-4 opens with `OBSERVATION`. Each minute: submit-OK, attempts, rejects split into rate and full, and the waiting count (submitted-OK not yet landed) for each cohort. Each public node: a local number, synced, DAA, submit-OK, rejects, dropped sockets, answer time. Per cohort, per target: the submit-to-landing median and the slow tail. An id used to match stays off the repo.

Call git by its full path. Empty output is a failed read. Read once more. One commit per file. If the push fails, try once more, then stop and say the git error. You do not write `counts/mini/` or `counts/bot/`.

When RETURN is on origin, met or `NOT MET`, stop the families and the payments. Write [logs/METHOD.md](logs/README.md). If a fix worked, append it to [locks/LOCKED.md](locks/LOCKED.md) in the form that page shows. Do not rewrite this paste. Then one commit on tn-master for this pre-run's row only. Do not change Wednesday's row into a result from this pre-run.

Abort line **2,500 coins** and **18,000 usable tKAS**. Do not lower it. Do not print a balance. Do not spend a coin at or above 100,000 tKAS.

## What you refuse

- Sending before 23:00 CET (22:00 UTC) on 10 Nov 2026, or while a Tuesday runner is up.
- Stopping the desk node, deleting chain data, or switching the binary.
- Editing the Tuesday repo or the Wednesday repo, or writing `REVIEW_CLOSED`.
- A second runner, or a waiter that sits until the gate.
- Bringing the bot in on a scored offer.
- An id, a txid, a key, a seed, an address, a host, or a port in this repo or in chat.
- Rewriting this page after the paste to match the result.
