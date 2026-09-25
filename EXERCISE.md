# Exercise: add your own SKILL.md

Write a small reusable instruction set for a real task, such as checking a CSV header, summarizing an issue, or reviewing a dataset card. This exercise is for learning; submit only after a maintainer confirms the repo is ready to accept exercise PRs.

1. Pick a task you can demonstrate with a harmless sample input and output. Write a one-sentence success test.
2. Create `skills/<your-skill-name>/SKILL.md`. The folder name and YAML `name` must match: 1-64 lowercase letters, digits and hyphens; no leading/trailing or doubled hyphens.
3. Add YAML frontmatter with required `name` and `description` (nonempty, max 1024 characters, describing both purpose and when to use it). Put Markdown instructions below the closing `---`. Optional `license`, `compatibility`, `metadata` and `allowed-tools` are described in the specification. Do not claim tools you cannot test.
4. Include steps, a sample input and expected result, and at least one edge case. Test them yourself. Do not put secrets, personal data, or instructions to send or change things without permission in the skill.
5. Check your folder and file against https://agentskills.io/specification. If you have `skills-ref`, run `skills-ref validate ./skills/<your-skill-name>`; otherwise use the checklist above and state that automatic validation was not run.
6. Ask the organizer whether to open a PR. In the PR, explain the task, your test, and what you changed after testing.

Starter shape (replace every placeholder; do not submit this template unchanged):

```markdown
---
name: sample-task
description: Checks a sample input for a clearly stated condition. Use when reviewing that input before sharing it.
---

# Sample task

1. Read the input.
2. Check the required condition.
3. Report the result and any missing information without inventing it.

Example input: ...
Expected result: ...
Edge case: ...
```
