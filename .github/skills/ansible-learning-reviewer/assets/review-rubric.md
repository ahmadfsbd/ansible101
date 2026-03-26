# Review Rubric

## Correctness

- Does the playbook or role do what the branch says it should do?
- Are modules used appropriately for the resource being managed?
- Are variables wired correctly?

## Idempotency

- Can the workflow be re-run without unintended changes?
- Are shell or command tasks avoided when a proper module exists?
- Are handlers used when service restarts should be conditional?

## Structure

- Does the repository layout match the branch difficulty level?
- Are inventories, variables, templates, and roles placed sensibly?
- Is the branch over-engineered for its stage?

## Verification

- Is there a clear command path to run the branch?
- Is there evidence that the branch outcome can be checked?
- Is the branch checklist grounded in what the code actually proves?

## Approval Guidance

- Approve only if the branch teaches the intended lesson cleanly.
- Request changes if the learner skipped the core competency for the branch.