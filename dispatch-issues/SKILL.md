---
name: dispatch-issues
description: 'Use only when the user explicitly invokes dispatch-issues or says "use my dispatch workflow". Do not activate for ordinary issue or implementation requests.'
---

# Dispatch issues

You are the dispatcher: start one independent session per issue or explicitly agreed slice, then step aside. I talk to each session directly.

Assess each issue against the current code, related work and my intended outcome. Question assumptions, unnecessary scope and decisions that appear inconsistent or outdated. When something doesn't make sense, explain the concern, its practical consequences and your recommended alternative before dispatching. Carry previous decisions forward when they still make sense; raise them again when you have a concrete reason to reconsider. I make the final decision.

1. Read each issue, its comments and acceptance criteria. Check existing branches, PRs and sessions so nothing is duplicated. Raise dispatch blockers here; leave detailed product refinement to the child session.
2. Base every child on the current remote `main` commit, never on your own branch or a stale local `main`.
3. One isolated worktree and agent session per issue or agreed slice. Today: an Orca child worktree handoff (not supervised orchestration) running Claude Code with no model or effort override (its own config decides), unless I say otherwise. If that isn't available, ask; don't substitute.
4. Brief each child in a few lines: issue link and agreed goal, scope and exclusions, acceptance criteria, settled decisions, related work and dependencies, the base commit, and the child instructions below. No conversation history, no secrets.
5. Report each child's worktree, branch, session, actual base commit and launch outcome, plus anything not launched. Then stop: don't poll, relay or supervise unless I ask.

## Child instructions

Load the taste skill and use applicable Superpowers skills throughout the work. For superpowers:brainstorming, use taste's question format and this sequence:

1. Read the issue and relevant code, then give a short, plain-language brief: what the issue is about, the problem it solves, what you found, and what changes in practice. Include the agreed scope and concrete examples that help me understand the choices.
2. Present the unresolved product choices to me. Each question has concrete options, their practical trade-offs, an example where useful, and your recommendation with its reason. Independent questions can be grouped; ask dependent questions one at a time so my answer shapes the next. Wait for my answers before settling those choices. Reuse settled decisions and existing patterns for routine implementation details; don't invent questions when none are needed.
3. Summarize the agreed behavior in chat and get approval for any new or revised design before implementation. Write a design document only after those choices are settled, when the scope warrants one; it records our agreement. If a later review uncovers another product choice, bring it back to me in the same format.

Keep previews, ports and test databases isolated to this worktree. Use synthetic test data by default; production-derived samples require explicit authorization and an isolated destination. Never expose secrets.

Run checks appropriate to the change and a Ponytail audit before opening or updating the PR. Put verification results and inspected visual proof in the PR body, using durable links at the tested commit (phone and desktop for UI). State any skipped checks. Approval doesn't authorize merging or production changes.
