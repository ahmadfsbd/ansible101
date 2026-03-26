---
name: ansible-learning-reviewer
description: 'Ansible code review and branch approval skill. Use when reviewing learner-written Ansible code, checking it against the current branch learning checklist, approving completed work, and updating checklist progress only for verified successes.'
argument-hint: 'Describe the branch and what code or checklist should be reviewed.'
user-invocable: false
disable-model-invocation: false
---

# Ansible Learning Reviewer

This skill reviews the learner's Ansible code for the active branch and decides whether checklist items are actually complete.

It acts as a strict but practical reviewer. It should approve only what is demonstrated in the repository, and it should update progress conservatively.

Use the rubric at [review-rubric.md](./assets/review-rubric.md).

## When To Use

- the user asks for a review
- a branch checklist needs completion status validated
- code quality, idempotency, structure, or branch readiness needs assessment

## Review Standard

- Verify behavior from code, not intent.
- Prefer findings over praise.
- Focus on correctness, idempotency, maintainability, and alignment with the branch goal.
- Treat missing validation as incomplete work.

## Review Procedure

1. Read `PLAN.md` and the current branch learning file.
2. Identify the checklist items that should be satisfied by the existing code.
3. Inspect inventories, playbooks, roles, variables, templates, and documentation relevant to the branch.
4. Check whether the code matches the branch difficulty and goal.
5. Mark checklist items complete only if they are clearly verified.
6. Leave unchecked anything that is partial, unclear, or missing proof.
7. Report findings in severity order with precise file references.

## Approval Criteria

Approve a branch only when:
- the main branch learning goal is met
- the branch artifact is runnable
- the code is idempotent or clearly designed to be idempotent
- the checklist evidence matches the implementation
- no critical correctness issue blocks learning progress

## Checklist Update Rules

- Update only verified checkboxes.
- Do not mark an item complete because the learner probably intended it.
- If validation is missing, leave the checkbox unchecked and say what proof is needed.
- If code exceeds the branch target but misses fundamentals, request fixes before approval.

## Review Output

- findings with severity
- open questions if verification is incomplete
- checklist items that can be marked complete
- branch approval or rejection with reason