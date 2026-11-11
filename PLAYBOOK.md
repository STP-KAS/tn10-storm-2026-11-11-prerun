> **Experimental. We are just trying this.** [Disclaimer](DISCLAIMER.md) · Kaspa Testnet-10 only; tKAS has no value.
>
> **This is the playbook map for pre-run 1**, the 11 Nov 2026 rehearsal. It is not Wednesday. It is not Tuesday. It does not start a machine and it does not arm one. A read of this page is not a paste.

# Playbook map

This page has two jobs. It records what went wrong in pre-run 1, where it happened, and how it was handled. It also states who does what, and when each machine may start, so Mini, the desk (Build), and the bot do not guess.

The plan stays in [plan/PLAN.md](plan/PLAN.md), [locks/LOCKED.md](locks/LOCKED.md), and the three go files. This page does not rewrite those pastes. The next attempt, if opened, is a new repo, `tn10-storm-2026-11-11-prerun-2`, and it starts from the lock file.

## Oversight

TN10 ops oversees this rehearsal end to end: Mini, the desk (Build), and the bot.

On 11 Nov 2026, after the desk and Mini reset, the operator gave TN10 ops full PowerShell admin on Mini and the desk, and asked it to restart the stack, watch the situation, and do what the plan needs, not only the nodes. That includes senders, whether hash files land on origin, count files, disk, and start gates. TN10 only. Never mainnet. Keep disk safe. Do not edit the Tuesday repo or the Wednesday repo. Do not write `REVIEW_CLOSED`.

The operator still sends the three pastes. That send is the arm. Oversight does not arm a machine by itself.

What oversight checks, on this run and the next:

- Nodes: the existing TN10 process is the one that is up, data is not wiped, the node is synced before we count or send, and the desk devnet is left alone.
- Hashes: sixteen family rows are on origin, with an On origin line, before the first family submit. No On origin line, no send. The covenant id stays off the repo.
- Senders: one family-sender on the desk, payments only as the plan allows, the bot only in the HOLD-4 minute on a leftover synced public node, or a legal `NO SEND`. No second runner.
- Files: desk, Mini, and bot each write only their own folder. HOLD-4 is the pinned minute after desk HOLD-3 is on origin.
- Start gates: no send or count before the gate in this page and in the go files.
- Disk and abort: do not start if the lane would fall under 2,500 coins or 18,000 usable tKAS. Do not print balances or secrets.

## Who does what, and when to start

[GO.md](GO.md) is still the paste map. The operator pastes the file that names the machine in front of him.

| Who | Role | When to start | What not to do |
|---|---|---|---|
| **Desk (Build)** | Sends the sixteen families and the payment offers. Does not count the chain. Publishes `logs/PRE-RUN-OPEN.md` when the start gate is open, then the hash file, then `counts/desk/` as each step closes. | Only after the operator pastes [GO-DESK.md](GO-DESK.md), the start time has passed, Tuesday's runner is down, and the lane is above the abort line. For a new attempt after this failure: also only after Mini has re-synced and has notified Build. First sentence must be: `DESK. I send on the pre-run. I do not count. This is not Wednesday.` | Do not start a runner from a chat sentence. Do not count. Do not stop the desk TN10 node as part of the pre-run. Do not drop a HOLD-3 node to free one for the bot. Do not edit Tuesday's or Wednesday's repo. Do not start a second runner. |
| **Mini** | The only chain counter. Does not send. Does not mine. Does not hold a key. Publishes `logs/MINI-ARMED.md` after `PRE-RUN-OPEN` is on origin, then `counts/mini/` when the matching desk file is on origin. | After this failure, and before any new paste: start the existing TN10 kaspad if it is down, do not wipe chain data, and re-sync first. When the node is genuinely synced (`isSynced` true, DAA moving), notify Build and TN10 ops. Do not arm, count, or publish a new `MINI-ARMED` until the operator pastes [GO-MINI.md](GO-MINI.md) and `PRE-RUN-OPEN` is on origin. First sentence of that paste: `MINI. I count the pre-run. I do not send. This is not Wednesday.` | Do not send. Do not start a counter before the gate file. Do not resume pre-run 1. Do not start the pre-run or Tuesday runner tasks on a failed run. Do not edit Tuesday's or Wednesday's repo. |
| **Bot (TN10 ops)** | Sends payments in the HOLD-4 minute only, on one leftover synced public node outside the desk HOLD-3 set, or publishes a legal `NO SEND`. Publishes `counts/bot/HOLD-4.md`. Does not count the chain. | Only after the operator pastes [GO-BOT.md](GO-BOT.md), `PRE-RUN-OPEN` is on origin, and desk `counts/desk/HOLD-3.md` is on origin. Send only in the pinned HOLD-4 minute. First sentence must be: `GROKBOT. I send payments on the pre-run HOLD-4 only. I do not count. This is not Wednesday.` Stop at once on `logs/BOT-HALT.md`. | Do not send on HOLD-1, HOLD-2, HOLD-3, or RETURN. Do not start a second waiter or runner. Do not treat chat as the start signal. Origin files are the signal. |

A sentence in chat is not `PRE-RUN-OPEN`, not an arm, and not a send order. The operator's paste is the arm.

## What happened in pre-run 1

Pre-run 1 is marked failed. The note is [logs/FAILED.md](logs/FAILED.md). The bot stop line is [logs/BOT-HALT.md](logs/BOT-HALT.md).

The start had passed, and Tuesday's runner was down.

- Desk published [logs/PRE-RUN-OPEN.md](logs/PRE-RUN-OPEN.md) at 2026-11-10T23:05:11Z (00:05:11 Brussels), commit dd38ec9.
- Mini published [logs/MINI-ARMED.md](logs/MINI-ARMED.md) at 2026-11-10T23:15:29Z (00:15:29 Brussels), commit 0dc3c0c.
- The bot waiter was already polling origin for `PRE-RUN-OPEN` and desk HOLD-3. It first saw the open file at 00:05:30 Brussels.

No hash file was published. No desk, Mini, or bot count file was published. There was no HOLD-1, HOLD-2, HOLD-3, HOLD-4, or RETURN on origin. The bot did not send.

During the night the desk and Mini reset. After that, nothing was armed for send.

## Issues, where, and how they were handled

Times below are Brussels local, with the UTC stamp where it matters. Status is as of 2026-11-11T07:35:00Z (08:35 Brussels).

| Issue | Where | What happened | How it was handled | Status |
|---|---|---|---|---|
| Desk reset mid-run | Desk | The desk last booted at 01:31 on 11 Nov 2026. After the reboot, no kaspad, miner, or sender was running. No hash file and no desk count file had been published. | Pre-run 1 was not resumed. It was marked failed. The desk TN10 node was not wiped. It has not been restarted yet. The desk devnet is left alone. | Open. The desk node is still down. |
| Mini reset mid-run | Mini | Mini last booted at 02:48 on 11 Nov 2026. After the reboot it was unreachable in the app, so processes could not be read and the machine could not be disarmed from here. | Pre-run 1 was not resumed. No new `MINI-ARMED` was written. The historical `MINI-ARMED` file was left in place as a record of the failed run. | Reachability solved later that morning. Sync is a separate row. |
| Mini unreachable after the reboot | Mini | Until 08:29 the Mini machine showed disconnected, so kaspad could not be started or inspected. | At 08:29 the operator said Mini was on. The machine was reachable again. | Solved. |
| Mini TN10 node down after the reboot | Mini | No kaspad was running when Mini came back. Existing chain data was still in place. | At 08:31 the existing TN10 start task was used. kaspad 2.1.0 came up on testnet-10 with the existing data directory, `--ram-scale=0.4`, and no wipe. IBD started, with peers connected and headers moving from the existing pruning point. No miner, counter, pre-run runner, or Tuesday runner was started. | In progress. At 08:33 the header IBD was at about 22% and still unsynced. When it is genuinely synced, Mini notifies Build and TN10 ops. |
| Bot waiter still polling a dead run | Bot | The bot waiter, started 10 Nov at 23:06, was still polling at 08:16:04 with `PRE-RUN-OPEN` present and desk HOLD-3 absent. If a HOLD-3 file had appeared after the machines died, it might have tried to send. | The operator stopped all arming. The waiter was stopped at 08:16:33. It had not sent. [logs/BOT-HALT.md](logs/BOT-HALT.md) records that stop (`BOT_HALT 2026-11-11T07:16:33Z`). No second waiter was started. | Solved. The bot is not sending. |
| Pre-run 1 could not be completed | Desk, Mini, and bot | The machines reset before hashes or sends. Nothing was armed for send afterwards. | Logged in [logs/FAILED.md](logs/FAILED.md) at commit addda90 (08:21:32 Brussels, 2026-11-11T07:21:32Z). This repo's pastes were not rewritten. Tuesday's repo and Wednesday's repo were not edited. | Failed, closed. The next attempt is a new repo if one is opened. |
| Risk of arming or starting a leftover runner | Mini and bot | Mini still had scheduled pre-run and Tuesday runner tasks present, enabled, and not running. A second bot waiter would have been a fault. | Those runner tasks were left alone and not started. No second bot waiter was started. No machine was armed. The three pastes will only be given when a new run is actually ready. | Solved for this close-out. Do the same on the next attempt. |
| Hashes and senders never got a reading | Desk, then Mini and bot | Because the run died before `hashes/SIXTEEN.md` and before any submit, there is no landing check and no sender repair to record. This is a miss of the run, not a fee or rate finding. | Recorded here so the next attempt still checks them: On origin hashes before the first submit, submit-OK and rejects on the desk, Mini's hop counts against those hashes, and the bot only in the pinned HOLD-4 minute. | Not exercised. Must be checked on the next attempt. |
| Wednesday clock is the same day | All | Wednesday's neuron is still [tn10-storm-2026-11-11](https://github.com/STP-KAS/tn10-storm-2026-11-11), T0 12:00 UTC / 13:00 Brussels on 11 Nov 2026. A full new pre-run needs Mini synced first and may not fit before that clock. | No prerun-2 repo was opened at this writing. Wednesday was not armed. `REVIEW_CLOSED` was not written. Oversight will not arm a new pre-run until Mini is synced, Build has been notified, and the window is clear. | Open. Do not squeeze a new pre-run into Wednesday's clock without a clear window. |
| Mini TN10 node re-sync finished | Mini | The existing kaspad 2.1.0 on testnet-10, started at 08:31:03 from the existing data directory with `--ram-scale=0.4` and no wipe, was still in IBD at the last row. | IBD completed at 09:04:08 (2026-11-11T08:04:08Z). The node then accepted live blocks by relay, and was still doing so at 11:00. No miner, counter, pre-run runner, or Tuesday runner was started. Peer addresses stay off this repo. | Solved. Mini's node is live. Pre-run 1 is still not resumed. |
| Desk TN10 node down after the reboot | Desk | After the 01:31 reboot no kaspad was running on the desk. Windows PowerShell 5.1 drops the start arguments and can open mainnet. | At 08:44:58 (2026-11-11T07:44:58Z) the existing private TN10 kaspad 2.1.0 was started from its existing data, loopback only, with PowerShell 7 (`pwsh`). No wipe. `KaspaPublicNode` was not started. The desk devnet was left alone. IBD finished at 08:54:58 (2026-11-11T07:54:58Z). It was still accepting live blocks at 11:01. | Solved. The desk node is live. |
| Box TN10 node | Bot (box) | The box node was not brought back. | Given up. There is no local TN10 node on the box, which matches the lock that the bot has no local node. Box miners are stopped. No bot waiter is running. | Closed. |
| Same-day clock for a new attempt | All | A new attempt on a wall clock would race the day and leave a waiter sitting on a time. | The operator postponed today's run and said the next attempt is target-oriented, with no time frames (10:59 Brussels, 2026-11-11T09:59Z). The next attempt is the new repo [tn10-storm-2026-11-11-prerun-2](https://github.com/STP-KAS/tn10-storm-2026-11-11-prerun-2), with no T0 and no public clock. Wednesday was not armed. `REVIEW_CLOSED` was not written. | Solved by the new repo. This repo stays failed and closed. |
| Hash publisher has no sixteen-family mode | Desk | The desk hash tools publish only 8 or 32 families. Pre-run 2 needs `hashes/SIXTEEN.md` with sixteen rows and an On origin line before any family submit. | The 8- and 32-family publisher is not used for the pre-run. A sixteen-family path is needed before any hash file is published. No hash file was invented. | Open. Carried to pre-run 2 as its first target. |

## What happens next

1. Mini finishes the re-sync of the existing TN10 node. No wipe. When `isSynced` is true and DAA is moving, Mini notifies Build and TN10 ops.
2. Oversight keeps watching Mini, the desk, and the bot. The desk TN10 node is still down and is a later step, without touching the desk devnet.
3. The three armings — [GO-DESK.md](GO-DESK.md), [GO-MINI.md](GO-MINI.md), and [GO-BOT.md](GO-BOT.md) — are given only when a new run is ready. They are not given now.
4. If a new attempt is opened, it is `tn10-storm-2026-11-11-prerun-2`, starting from [locks/LOCKED.md](locks/LOCKED.md), with this playbook's Mini re-sync-then-notify-Build step baked into that repo's own pastes. This repo's go files stay as they were.

When a later issue is solved, append a row to the table above, or append a worked fix to [locks/LOCKED.md](locks/LOCKED.md) in the form that page already shows. Do not rewrite the go files in this repo to match the result.
