# Kit-v1 validation plan

The stripped system is not better because it has fewer files. It is better only if it retains the useful behaviour of the old system with less complexity.

## Test A — fresh-session routing

Start a new Claude Code session in Kit-v1 with no additional explanation.

Ask:
- Who am I?
- What is my current priority?
- Where should a new project live?
- Where should detailed task-specific procedure go if it becomes repeatable?
- Should you load every research file before answering a normal project question?

Pass:
- correct paths;
- no invented facts;
- no whole-repo preload;
- identifies Skill as an earned addition rather than assuming one already exists.

## Test B — real project

Create one representative project with:
- a clear outcome;
- a small amount of project context;
- an observable finish condition.

Ask Claude to complete it.

Pass:
- reads only relevant project/context files;
- defines or follows the finish condition;
- produces the actual deliverable;
- verifies the result before claiming completion.

## Test C — correction persistence

Correct Claude on one project-level behaviour.

Pass:
- Claude decides whether the correction belongs in project context, root instructions, a scoped rule or auto memory;
- it does not automatically bloat AGENTS.md.

## Test D — repeated workflow

Repeat the same multi-step process enough times that procedural duplication is obvious.

Pass:
- only then create a Skill;
- the Skill holds task procedure that would otherwise pollute root instructions.

## Test E — isolated work

Give a task with two independent research/implementation branches.

Pass:
- use a subagent/worktree only when isolation or parallelism adds value;
- no permanent role architecture is created.

## Test F — enforcement

Attempt a denied destructive command.

Pass:
- runtime blocks it independent of model judgment.

## Test G — native instruction audit

Run Claude Code's prompt audit against project instructions after the system evolves.

Pass:
- no stale paths, contradictions or instructions for obsolete features.

## Test H — long task continuity

Run a task long enough to cross normal session/context boundaries.

Pass:
- the project remains recoverable from durable task/project artifacts;
- add custom handoff machinery only if this fails.

## Comparison with Test-environment-

Measure both systems on:
- always-loaded instruction size;
- number of root concepts a beginner must understand;
- files read before useful work begins;
- task completion;
- verification quality;
- correction persistence;
- continuity;
- hard safety controls.

Promotion condition:

Kit-v1 must match or improve outcome quality on representative tasks while requiring less always-loaded context and fewer custom mechanisms.
