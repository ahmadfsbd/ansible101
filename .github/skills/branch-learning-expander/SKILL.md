---
name: branch-learning-expander
description: 'Branch planning skill for this Ansible learning repo. Use when a new branch is created from main and needs to be mapped to the progression in PLAN.md, then expanded into a branch-specific learning markdown file with checklists and practical tasks.'
argument-hint: 'Provide the branch name to map and expand.'
user-invocable: false
disable-model-invocation: false
---

# Branch Learning Expander

This skill creates or updates the branch-specific learning guide for a newly created learning branch.

Its job is to inspect the branch name, compare it against the sequence in `PLAN.md`, and produce a learning file that translates the branch goal into actionable tasks and verifiable checkpoints.

Use the template at [branch-learning-template.md](./assets/branch-learning-template.md).

## When To Use

- a new branch is created from `main`
- a branch exists but does not yet have its own learning checklist
- the branch learning file needs to be expanded from a short outline into a workable path

## Inputs

- branch name
- `PLAN.md`
- any existing file under `branches/` for that branch

## Procedure

1. Read `PLAN.md`.
2. Match the branch name to the closest stage in the progression.
3. Identify the intended difficulty jump from the previous branch.
4. List branch prerequisites before tasks, including required hosts, host groups, and target IP or DNS details.
5. Create or update a branch learning file under `branches/`.
6. Use checklist items that can be reviewed against actual code or runnable commands.
7. Separate checklist items into:
   - setup
   - build tasks
   - verification
   - reflection
8. Include success criteria and a clear definition of done.

## Checklist Rules

- Every item should be specific enough to verify.
- Prefer action verbs such as install, create, configure, template, run, validate.
- Add a prerequisites section that names required hosts and expected IPs (or DNS names) for the branch.
- Include at least one idempotency check on every branch.
- Include at least one command or execution path that proves the branch works.
- Avoid vague items such as understand Ansible better.

## Naming Rules

- Branch learning files should follow the branch name when practical.
- If the branch already has a file, update it rather than creating duplicates.
- Keep the content aligned with the order defined in `PLAN.md`.

## Output Standard

The generated branch file should give the learner:
- the branch goal
- why it matters
- prerequisites for hosts, host groups, and IP or DNS targets
- a practical project structure
- a checklist of tasks
- a checklist of validation steps
- completion criteria