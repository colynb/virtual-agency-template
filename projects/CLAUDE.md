# Project Management

Each active project gets its own folder here. Projects are time-bound, goal-oriented efforts that reference knowledge base concepts but have their own lifecycle.

## Creating a Project

1. Copy `projects/_template/` to `projects/<project-slug>/`
2. Fill in `brief.md` with the project goals, scope, and stakeholders
3. Initialize `status.md` with the current state
4. Start `log.md` with the first entry
5. Log the project creation in `logs/activity.md`

## Project Structure

```
projects/<project-slug>/
├── brief.md      # Goals, scope, constraints, success criteria
├── status.md     # Current state, blockers, next steps
└── log.md        # Chronological record of decisions and progress
```

## Conventions

- Update `status.md` whenever significant progress is made
- Log important decisions in both `log.md` and `logs/decisions.md`
- Reference knowledge base concepts by linking to their files: `[Concept](../../knowledge/concepts/slug.md)`
- When a project is complete, move it to `projects/_archive/` (create that folder if needed)
