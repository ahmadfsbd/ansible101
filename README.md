# Ansible101

A branch-based, practical Ansible learning repository.

The goal is to learn Ansible from scratch and progress toward realistic project structures, review discipline, and repeatable automation habits.

## Learning Model

- Main branch holds the roadmap and shared learning guidance.
- Each learning branch starts from main.
- Skills are cumulative across branches, while branch code stays clean and stage-specific.
- Every branch should end with something runnable.

Read the high-level roadmap in `PLAN.md`.

## Repository Structure

```text
ansible101/
├── .github/
│   └── skills/
│       ├── ansible-learning-master/
│       ├── ansible-learning-mentor/
│       ├── ansible-learning-reviewer/
│       └── branch-learning-expander/
├── branches/
│   └── 01-foundations.md
├── PLAN.md
└── README.md
```

## Skill Roles

### 1) Master Orchestrator

- Skill: `ansible-learning-master`
- Purpose: route requests to the right specialist skill based on current need.

### 2) Mentor

- Skill: `ansible-learning-mentor`
- Purpose: refine branch learning steps so they stay realistic, practical, and appropriately scoped.

### 3) Branch Expander

- Skill: `branch-learning-expander`
- Purpose: when a new branch is created from main, map it to `PLAN.md` progression and create or expand a branch-specific checklist file under `branches/`.

### 4) Reviewer

- Skill: `ansible-learning-reviewer`
- Purpose: review learner-written code against branch goals and checklists, and mark completion only for verified items.

## How To Use This Repo

### Step 1: Pick The Next Branch From PLAN

- Open `PLAN.md`
- Choose the next branch stage in order

### Step 2: Create The Branch From Main

Example:

```bash
git checkout main
git pull origin main
git checkout -b 01-foundations
```

### Step 3: Expand Branch Learning File

- Use the branch expander workflow to create or refine the branch learning checklist under `branches/`.
- Keep tasks concrete and verifiable.

### Step 4: Build The Branch Project

- Implement the project structure and playbooks for that stage.
- Keep scope focused on the branch goal.

### Step 5: Review Before Promotion

- Run the reviewer workflow against code and checklist.
- Mark only verified items complete.
- Fix gaps before moving to the next branch stage.

## First Stage

Start with `01-foundations` using the guide in `branches/01-foundations.md`.

## Success Criteria For The Overall Path

- You can explain why each branch exists.
- You can run each branch artifact end-to-end.
- You can demonstrate idempotent Ansible behavior on every branch.
- You can pass branch review with checklist evidence.

## Notes

- Keep branch complexity incremental.
- Avoid jumping ahead before the current stage feels intuitive.
- Prefer practical examples over toy-only tasks.
