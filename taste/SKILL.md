---
name: taste
description: Eduardo's taste for building software. Load before planning, writing or reviewing code, and before asking him to decide anything.
---

# Taste

## Code

1. Does it need to exist? Build for the problem we have now. Fewest moving parts; ship the thin version, defer the rest.
2. Least custom code. Use the tool's defaults and generators, an official plugin, a service already in use, or a maintained, widely used library before writing your own.
3. Search the repo before adding anything. Reuse it, never duplicate, keep one source of truth.
4. Simple code, never a simplistic product. Half-done isn't done, and the UI is smooth and refined: nothing breaks, blinks or jumps at phone or desktop width.
5. Every line in the diff serves the task: one concern per change, no drive-by edits, no narrating comments.
6. Delete what has done its job: one-off scripts, dead code, point-in-time docs.
7. Prove it, don't claim it: run it for real, put proof in the PR, and say what you verified versus what you assume.
8. Keep the repo agent-neutral: no rules, hooks or guides for one tool. A guardrail works for every agent, or it lives in my personal config, not the repo.

## Working with me

9. Size the effort to the task. Answer simple questions directly; save multi-agent workflows for complex or research-heavy work.
10. Evaluate, don't obey. Check specs, old decisions and my ideas against the code and real data; push back and recommend. I decide.
11. Starting from an issue, first explain it plainly: what it refers to, the goal, what changes in practice.
12. Ask only what you can't find out yourself, one question at a time: options, their trade-offs, and your recommendation. Never open-ended.
13. Issues and briefs you write say what and why, not how.
14. Prefer a tool's CLI or API to driving its web UI; use the browser when that's the only practical way.

## Tools (today, replaceable)

- Orca: a worktree and agent session per task, and a browser for page checks.
- Superpowers: brainstorm, spec, plan, build.
- ponytail: simplicity audit before a PR.
- GitHub (gh, gh-stack): issues, PRs, CI as the merge gate.
