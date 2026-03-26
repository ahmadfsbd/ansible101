# Ansible Learning Plan

This repository will be used as a step-by-step Ansible learning path.

## Repository Approach

- The main branch keeps the roadmap, notes, and shared reference material.
- Each learning branch introduces a more realistic project structure and a harder automation problem.
- Every branch should end with something runnable, not just notes.

## Branch Strategy

- Each learning branch should be created from `main`, not from the previous learning branch.
- The learning progression is cumulative in skills, not in inherited branch code.
- Each branch should reuse concepts from earlier branches while allowing the project structure to evolve for that stage.
- This keeps branches clean while still making the overall path progressively more realistic.

## Progression

### 1. Foundations

Branch: `01-foundations`

Focus:
- Install and verify Ansible
- Understand inventory basics
- Run ad-hoc commands
- Write first playbooks
- Use variables and simple tasks

Build outcome:
- A minimal Ansible project that targets `localhost`
- A few basic playbooks for connectivity, packages, files, and services

### 2. Roles And Reuse

Branch: `02-roles-and-reuse`

Focus:
- Break playbooks into roles
- Use defaults, vars, handlers, and templates
- Improve project layout

Build outcome:
- A reusable role-based setup for a simple service such as Nginx or Docker

### 3. Multi-Host Management

Branch: `03-multi-host`

Focus:
- Multiple hosts and groups
- Group variables and host variables
- Different behavior per environment

Build outcome:
- One project that configures several hosts with different responsibilities

### 4. Idempotent App Setup

Branch: `04-app-deployment`

Focus:
- Deploy an application stack
- Manage configuration files from templates
- Validate idempotent runs

Build outcome:
- A complete service deployment with repeatable playbook runs

### 5. Secrets, Vault, And Safer Operations

Branch: `05-secrets-and-ops`

Focus:
- Use Ansible Vault
- Separate sensitive data
- Add tags and safer execution patterns

Build outcome:
- A more production-like structure with secure variables and targeted runs

### 6. Testing And Project Discipline

Branch: `06-testing-and-quality`

Focus:
- Linting and syntax checks
- Structured documentation
- Optional Molecule or CI integration

Build outcome:
- A maintainable Ansible repository with validation steps

## Working Rules

- Keep each branch focused on one learning jump.
- Prefer small, runnable examples before larger projects.
- Capture what was learned in a short branch README.
- Do not move to the next branch until the current branch feels intuitive.

## Immediate Next Step

Start with branch `01-foundations` and create a tiny local-only project that proves the basic Ansible workflow end to end.