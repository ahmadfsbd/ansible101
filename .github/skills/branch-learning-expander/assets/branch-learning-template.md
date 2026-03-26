# Branch {{branch_name}}

## Goal

State the exact competency this branch is meant to build.

## Why This Branch Matters

Explain how this branch moves the learner from the previous branch into more realistic Ansible work.

## Prerequisites

- Required hosts for this branch:
- Host groups to define in inventory:
- Expected IP addresses or DNS names:
- Connection assumptions (for example SSH user, key path, or localhost-only):

## Project Shape

List the expected repository structure, playbooks, inventories, roles, or variable files that should exist by the end.

## Checklist

- [ ] Create or update the inventory needed for this branch.
- [ ] Add the playbook, role, or project files required for the branch goal.
- [ ] Use variables in a way that matches the branch target.
- [ ] Run the branch workflow successfully.
- [ ] Re-run and confirm idempotent behavior.

## Validation

- [ ] Run the main playbook or command path for this branch.
- [ ] Verify the expected managed state on the target host or localhost.
- [ ] Confirm the result matches the intended branch outcome.

## Definition Of Done

- The branch artifact is runnable.
- The checklist items are reviewable from code and execution evidence.
- The branch clearly prepares for the next stage in `PLAN.md`.