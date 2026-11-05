---
name: taste
description: Eduardo's taste for building software. Load before planning, writing or reviewing code, and before asking him to decide anything.
---

# Taste

## Code

1. Does it need to exist? Build for the problem we have now. Fewest moving parts; ship the thin version, defer the rest.
2. Least custom code. Use the tool's defaults and generators, an official plugin, a service already in use, or a maintained, widely used library before writing your own.
3. Search the repo before adding anything. Reuse it, never duplicate, keep one source of truth.
4. Simple code, never a worse product. The UI is smooth and refined: nothing breaks, blinks or jumps at phone or desktop width.
5. Every line in the diff serves the task: one concern per change, no drive-by edits, no narrating comments.
6. Delete what has done its job: one-off scripts, dead code, point-in-time docs.
7. Prove it, don't claim it: run it on realistic data, show the result in the PR, and say what you verified versus what you assume.

## Working with me

8. Size the effort to the task. Answer simple questions directly; save multi-agent workflows for complex or research-heavy work.
9. Evaluate, don't obey. Check specs, old decisions and my ideas against the code and real data; push back and recommend. I decide.
10. Starting from an issue, first explain it plainly: what it refers to, the goal, what changes in practice.
11. Ask only what you can't find out yourself, as options with practical consequences and your recommendation. Never open-ended.
12. Issues and briefs you write say what and why, not how.

## Tools (today, replaceable)

Drive tools through their CLI or API, not a web UI.

- Orca: a worktree and agent session per task, and a browser for page checks.
- Claude Code: default implementer. Codex: when asked.
- Superpowers: brainstorm, spec, plan, build.
- ponytail: simplicity audit before a PR.
- GitHub (gh, gh-stack): issues, PRs, CI as the merge gate.
