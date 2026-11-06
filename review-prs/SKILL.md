---
name: review-prs
description: 'Use only when the user explicitly invokes review-prs or says "use my review workflow". Do not activate for ordinary review requests.'
---

# Review PRs

You are the coordinator: start one independent reviewer per PR, bring me the verdict, merge only on my word.

1. A review starts when I ask or, when I ask you to keep watching, whenever a PR becomes ready: open, not a draft, CI green, nothing pushed for ~10 minutes and its author session idle. Watch every PR in the repo and every layer of a stack, each head once; recheck on a timer with whatever your tool offers. Red CI is reported, not reviewed.
2. One isolated worktree and agent session per PR (per layer of a stack), checked out at the PR head. Today: a supervised Orca worker, so the report comes back, running Claude Code with no model or effort override, unless I say otherwise. If that isn't available, ask; don't substitute.
3. Brief each reviewer in a few lines: PR link, head and base commits, the linked issue, my settled decisions (not defects), open PRs it overlaps, and the reviewer instructions below. No conversation history, no secrets. Then wait for its report.
4. Report each verdict in plain words, in chat and as one comment on the PR pinned to the reviewed commit: Ready or Needs changes, what was verified, what blocks, what couldn't be checked, and where the full report is. A stack gets one line per layer.
5. Route findings. Blocking: to the PR's author session, then the same reviewer rechecks only the delta. Non-blocking: stay in the report until I say file them as issues (what and why). Product, privacy or cost calls, and a PR whose author session is gone: one question to me with a recommendation.
6. Merge only on my word (a batch "merge the ready ones" counts): a squash of the exact reviewed head with green CI; a stack merges as one. Anything touching production data waits for a per-case yes. Then confirm the deploy is live, delete what the review created, and leave other sessions' work alone.

## Reviewer instructions

Load the taste skill. Follow the repo's review guide (REVIEW.md at the root); without one, review against taste and a ponytail audit. Size the depth to the change and work alone: no sub-workflows. The PR body's claims and proof are claims to verify. Touch no shared or production data; run a migration only on a throwaway copy you delete. Say what you couldn't check instead of working around it. You only report: don't push, comment on GitHub or merge.
