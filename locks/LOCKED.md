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
- Families 1–13 and families 14–16 use the same family-sender nodes. Fees stay 100, 200, and 150 sompi per gram. The sixteen are one build. The rate is per family, in one process. A single rate for the process is not a fee difference. A second builder is not the fix. If the funding coins are not one size, the file says so and does not call the fee the whole cause. A priority quote is not read. A fee estimate is not read.
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

### Worked fixes appended on 11 Nov 2026, after pre-run 1 failed

These blocks are appended in the form above. The line `Nothing yet.` is the state before these blocks. Pre-run 2, [tn10-storm-2026-11-11-prerun-2](https://github.com/STP-KAS/tn10-storm-2026-11-11-prerun-2), starts from this page.

```
- 2026-11-11T07:21:32Z.
- What failed: the desk and Mini reset during pre-run 1, before hashes or sends. Nothing was armed for send after the reset.
- What was changed: pre-run 1 was marked failed in logs/FAILED.md and closed. It is not resumed. The next attempt is a new repo, tn10-storm-2026-11-11-prerun-2.
- Why that change stays: a failed pre-run's open and armed files are history, not live gates. A new attempt opens its own files in its own repo.
```

```
- 2026-11-11T07:16:33Z.
- What failed: the bot waiter from pre-run 1 kept polling origin after the desk and Mini had reset. A late HOLD-3 file could have made it send on a dead run.
- What was changed: the operator stopped the waiter. BOT-HALT was written. No second waiter was started.
- Why that change stays: a waiter does not outlive its run. When a run fails, its waiters are stopped and not reused. A new run gets a new paste.
```

```
- 2026-11-11T08:04:08Z.
- What failed: Mini rebooted during pre-run 1 and its TN10 kaspad was down.
- What was changed: the existing Mini TN10 kaspad was started with its existing start task and data directory. No wipe. It re-synced from its own data, finished IBD, and accepted live blocks.
- Why that change stays: before any new paste or arm, start the existing Mini TN10 kaspad if it is down. Do not wipe chain data. Re-sync first. When isSynced is true and DAA is moving, Mini notifies Build and TN10 ops. Mini does not publish a new MINI-ARMED until GO-MINI is pasted and PRE-RUN-OPEN is on origin.
```

```
- 2026-11-11T07:54:58Z.
- What failed: the desk rebooted during pre-run 1 and its private TN10 kaspad was down. Windows PowerShell 5.1 drops the start arguments and can open mainnet.
- What was changed: the existing desk private TN10 kaspad was started from its existing data, loopback only, with PowerShell 7 (pwsh). No wipe. KaspaPublicNode was not started. The desk devnet was left alone. IBD finished and the node accepted live blocks.
- Why that change stays: start the desk private TN10 node from existing data if it is down, with pwsh 7, never Windows PowerShell 5.1. Do not wipe. Do not start KaspaPublicNode. Leave the desk devnet alone. The pre-run does not stop the desk node process.
```

```
- 2026-11-11T09:59:00Z.
- What failed: pre-run 1 was gated on a wall clock and a waiter sat on that clock. The day's clock moved and the run died before hashes.
- What was changed: the operator set the next attempt as target-oriented, with no time frames.
- Why that change stays: the pre-run is target-bounded. It has no T0 after the start and no public clock. Order: hashes first (hashes/SIXTEEN.md, sixteen rows, with an On origin line), then covenant families, then gradual senders. The bot sends only in the HOLD-4 minute after desk HOLD-3 is on origin, or writes a legal NO SEND. Chat is not the start signal. The operator's paste is the arm.
```

```
- 2026-11-11T10:00:00Z.
- What failed: the desk hash tools publish only 8 or 32 families. The pre-run needs sixteen.
- What was changed: the old 8- and 32-family publisher is barred for the pre-run. A sixteen-family path is needed before any hash file is published. No hash value or covenant id is invented.
- Why that change stays: a hash file with the wrong family count is not proof. No sixteen-row file with an On origin line, no family submit.
```
