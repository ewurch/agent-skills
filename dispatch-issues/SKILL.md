---
name: dispatch-issues
description: 'Use only when Eduardo explicitly invokes dispatch-issues or says "use my dispatch workflow". Do not activate for ordinary issue or implementation requests.'
---

# Dispatch issues

Act as Eduardo's dispatcher. Launch independent sessions, then hand control to him.

1. Load the installed `orca-cli` skill and its version-matched guide from the selected Orca executable before Orca actions. Use direct child worktree/agent handoffs. Do not create supervised orchestration, ask/reply routing, notifications, monitors, or a task registry.
2. Read the requested issues, comments, and acceptance criteria. Check existing branches, PRs, worktrees/sessions, and dependencies to avoid duplicate work. Surface conflicts or missing dispatch inputs directly to Eduardo here. Include dependencies in briefs; dependent children may brainstorm now but must resolve prerequisites with Eduardo before dependent implementation.
3. Verify the intended repository and current remote `main` commit. Create one Orca child worktree and independent agent session per issue, explicitly based on that verified commit, preserving parent lineage. Never inherit the dispatcher's unmerged commits or use stale local `main` silently.
4. Default implementer: **Claude Code Opus 5.5, default effort**, unless Eduardo overrides it. Resolve the exact supported model identifier at launch; do not assume a moving `opus` alias means 5.5. Leave effort at its default. If unavailable, ask Eduardo here rather than substitute. The dispatcher's model and effort do not set child defaults.
5. Give each child a short, self-contained brief: issue ID/link and goal, acceptance criteria, relevant existing work and dependencies, verified base SHA, and the child instructions below. Do not copy conversation history or secrets. Confirm supported launch and prompt-delivery receipts; on ambiguous failure, reconcile the original operation before retrying to avoid duplicates.
6. List each issue, worktree/branch, session entry point or identifier, base SHA, model, and launch/prompt-delivery outcome, plus anything not launched. Then **stop**. Delivery is not implementation progress. Do not poll, supervise, relay child questions/status/approval requests, or coordinate across sessions unless Eduardo explicitly asks. Children speak directly with Eduardo in their own sessions.

## Include in every child brief

Start `superpowers:brainstorming`. Refine this issue directly with Eduardo in this session and obtain his approval before implementation. Do not send questions or approval requests through the dispatcher. After approval, follow the applicable Superpowers workflow; choose the simplest adequate implementation, run a `ponytail` audit, and meaningful tests. Keep previews, ports, and test databases isolated per worktree; never use production data or expose secrets. Before calling the PR ready, inspect durable visual proof and embed or link it in the PR body alongside the tested SHA and environment; UI work needs desktop and phone proof. For non-UI work, capture a relevant rendered test/API result. Use PR attachments or stable artifact links, not temporary local screenshot paths. Disclose missing proof or failed checks. Dispatch and design approval do not authorize merge or production actions.
