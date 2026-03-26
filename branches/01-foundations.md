# Branch 01: Foundations

Recommended branch name: `01-foundations`

## Goal

Learn the core Ansible workflow from scratch using only `localhost` first.

## Branch Position In The Roadmap

- This branch is intentionally minimal and focused on fundamentals.
- Future branches should be created from `main`, not from this branch.
- Later branches will reuse these skills while introducing more realistic project structures.

This branch should make these concepts feel normal:
- inventory
- modules
- playbooks
- variables
- idempotent execution

## What You Should Build

A minimal Ansible project with:
- a local inventory
- one or more simple playbooks
- a small variables file
- at least one task that creates or updates a file
- at least one task that installs a package or manages a service

## Suggested Project Structure

```text
ansible101/
├── inventories/
│   └── dev/
│       └── hosts.ini
├── playbooks/
│   ├── ping.yml
│   ├── setup.yml
│   └── files.yml
├── group_vars/
│   └── all.yml
└── README.md
```

## Concepts To Cover In This Branch

1. Install Ansible and verify it runs.
2. Create an inventory with `localhost`.
3. Run a simple ad-hoc command.
4. Write a playbook that uses `ansible.builtin.ping`.
5. Write a playbook that installs a package.
6. Write a playbook that creates a file with known content.
7. Re-run the playbook and confirm it is idempotent.

## Example Learning Tasks

- Ping `localhost` through Ansible.
- Install `curl` or another small package.
- Create a file under `/tmp` from a variable.
- Use `become: true` only where needed.
- Run in check mode and compare the result with a normal run.

## Success Criteria

You are ready for the next branch when you can explain and do all of the following without guessing:
- the difference between inventory and playbook
- what a module does
- why idempotency matters
- how variables are passed into tasks
- how to run a specific playbook against a specific inventory

## Notes For The Next Branch

Once this branch feels easy, the next step should be moving from loose playbooks into a role-based structure.