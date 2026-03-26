---
name: ansible-learning-master
description: 'Master orchestration skill for this Ansible learning repository. Use when coordinating branch-based Ansible learning, deciding which specialized skill should handle planning, branch expansion, realism refinement, or code review approval.'
argument-hint: 'Describe the branch or learning task that needs to be coordinated.'
user-invocable: true
disable-model-invocation: false
---

# Ansible Learning Master

This is the orchestration skill for the repository.

It does not do the teaching, branch expansion, or review work directly unless a lightweight routing response is enough. Its primary job is to identify the current stage in the learning progression and delegate the task to the most relevant specialized skill.

## When To Use

- A new learning branch is being created from main.
- A branch plan needs to be refined to feel more realistic.
- The user wants branch goals translated into a checklist.
- The user wants their Ansible code reviewed against the current learning target.
- The next best step in the progression needs to be decided.

## Delegation Rules

### Use `ansible-learning-mentor` when

- the overall progression needs to be refined
- a branch concept is too academic and should become more practical
- project scope should better resemble real Ansible work
- exercises need to become more production-shaped without becoming too advanced

### Use `branch-learning-expander` when

- a new branch has been created from main
- the branch name needs to be mapped to the learning progression in `PLAN.md`
- a branch-specific learning file with checklists should be created or updated

### Use `ansible-learning-reviewer` when

- the user asks for a review of code written on a learning branch
- completed tasks need to be checked against the branch checklist
- the branch learning file should be updated to reflect verified progress

## Operating Procedure

1. Read `PLAN.md` and identify the current stage of the learning progression.
2. Determine whether the request is orchestration, realism refinement, branch expansion, or review.
3. Route the task to exactly one specialized skill first.
4. If the branch scope changes after refinement, loop once through the mentor and then the branch expander.
5. If code review succeeds, let the reviewer update the learning checklist with only verified items.
6. Keep main focused on roadmap and branch-specific files focused on execution.

## Output Rules

- Keep branch progression aligned with `PLAN.md`.
- Do not invent branches that skip difficulty levels unless the user explicitly changes the plan.
- Prefer practical infrastructure tasks over toy examples.
- Each branch should produce a runnable Ansible project artifact.

## Repository Expectations

- `PLAN.md` is the source of truth for the sequence of branches.
- Branch-specific learning files should live under `branches/` unless the repository evolves a better convention later.
- Checklist updates should reflect actual reviewed work, not intent.