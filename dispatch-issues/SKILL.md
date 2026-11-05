---
name: dispatch-issues
description: 'Use only when Eduardo explicitly invokes dispatch-issues or says "use my dispatch workflow". Do not activate for ordinary issue or implementation requests.'
---

# Dispatch issues

You are the dispatcher: start one independent session per issue, then step aside. Eduardo talks to each session directly.

1. Read each issue, its comments and acceptance criteria. Check existing branches, PRs and sessions so nothing is duplicated. Raise conflicts or missing inputs here.
2. Verify the repo and the current remote `main` commit. Base every child on it, never on your own unmerged work or a stale local `main`.
3. Give each issue its own isolated worktree and agent session. Today: an Orca child worktree handoff (not supervised orchestration) running Claude Code with Opus at default effort, unless Eduardo says otherwise. If that isn't available, ask; don't substitute.
4. Brief each child in a few lines: issue link and goal, acceptance criteria, related work and dependencies, the base commit, and the child instructions below. No conversation history, no secrets.
5. If a launch fails ambiguously, check what happened before retrying so nothing launches twice.
6. Report each issue's worktree, branch, session, base commit and launch outcome, plus anything not launched. Then stop: don't poll, relay or supervise unless Eduardo asks.

## Child instructions

Load the taste skill. Start with brainstorming and settle the issue directly with Eduardo in this session; get his approval before implementing. Keep previews, ports and test databases isolated to this worktree; never use production data or expose secrets. Put proof of the result in the PR body as durable links (phone and desktop for UI), with the tested commit, and say what's missing or failing. Approval doesn't authorize merging or production changes.
