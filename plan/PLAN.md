> **Experimental. We are just trying this.** [Disclaimer](../DISCLAIMER.md) · This page does not start a machine. Pre-run 1. Not Wednesday. Not Tuesday.

# Targets

There is no T0. There is no latest minute. A scored target stays until three clean minutes land, or until one repair pass is done.

The start is 23:00 CET (22:00 UTC) on 10 Nov 2026. Before that hour, and while Tuesday's runner is up, nothing in this page starts.

| Order | Offer, tx/s | Who sends | File | Kind |
|---:|---:|---|---|---|
| 1 | 1,013 | desk | HOLD-1 | scored |
| 2 | 2,027 | desk | HOLD-2 | scored |
| 3 | 3,040 | desk | HOLD-3 | scored |
| 4 | 4,053 | desk, and the bot if a free synced node answers | HOLD-4 | observation |
| 5 | 1,013 | desk | RETURN | scored |

Sixteen families, offer 1.2 hop/s, boson, stagger 0, from the first send until RETURN closes. Families 1–13 pay 100 sompi/gram. Families 14–16 pay 200. Payments pay 150. Both cohorts use the same family-sender nodes.

A scored minute is clean when the desk's submit path is synced, that node's DAA is moving, submit-OK is within 10 percent, rejects are logged as rate or full, no sender-off, pool-low, node-drop, or proc-exit, and every family is still attempting. Mini's marks do not gate the next offer.

Payment senders use every public node that answers synced. One process per node. The desk keeps that set through HOLD-4.

HOLD-4 opens when the desk's HOLD-3 file is on origin, met or `NOT MET`. The sample minute is the first whole UTC minute whose start is at least 3 minutes after that file's On origin time. The rate in that minute is the reading, including a rate under 3,040. If the path is not synced, the file still covers that minute and says so. The run does not open a later minute.

The bot uses one public node outside the desk's HOLD-3 set. The split stays in the local config. The config is not committed. No free synced node means the bot does not send.

The abort line stays **2,500 coins** and **18,000 usable tKAS**. Do not lower it. Do not spend a coin at or above 100,000 tKAS. If this pre-run would leave the lane under that line for Tuesday or for Wednesday, do not start.

The Wednesday pages stay as they are. This page is the pre-run's page.

Locks: [locks/LOCKED.md](../locks/LOCKED.md).
