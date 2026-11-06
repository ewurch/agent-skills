---
name: dispatch-issues
description: 'Use only when Eduardo explicitly invokes dispatch-issues or says "use my dispatch workflow". Do not activate for ordinary issue or implementation requests.'
---

# Dispatch issues

You are the dispatcher: start one independent session per issue, then step aside. Eduardo talks to each session directly.

1. Read each issue, its comments and acceptance criteria. Check existing branches, PRs and sessions so nothing is duplicated. Raise conflicts or missing inputs here.
2. Base every child on the current remote `main` commit, never on your own branch or a stale local `main`.
3. One isolated worktree and agent session per issue. Today: an Orca child worktree handoff (not supervised orchestration) running Claude Code with no model or effort override (its own config decides), unless Eduardo says otherwise. If that isn't available, ask; don't substitute.
4. Brief each child in a few lines: issue link and goal, acceptance criteria, related work and dependencies, the base commit, and the child instructions below. No conversation history, no secrets.
5. Report each issue's worktree, branch, session, actual base commit and launch outcome, plus anything not launched. Then stop: don't poll, relay or supervise unless Eduardo asks.

## Child instructions

Load the taste skill. Brainstorm the issue with Eduardo in this session and get his approval before implementing. Keep previews, ports and test databases isolated to this worktree; never use production data or expose secrets. Proof in the PR is durable links (phone and desktop for UI) at the tested commit. Approval doesn't authorize merging or production changes.
