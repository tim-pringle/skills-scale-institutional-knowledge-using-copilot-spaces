# OctoAcme — Definition of Done (DoD)

## Purpose
Provide a shared, team-agreed checklist that every backlog item must satisfy before it is considered complete. Applying the DoD consistently reduces rework, prevents quality debt, and ensures releasable increments.

## When to use
- During sprint/iteration planning: confirm items in the backlog meet the DoD before pulling them into a sprint.
- During code review and QA: verify each criterion is met before moving a card to **Done**.
- During release readiness: the [Release Readiness Checklist](octoacme-release-readiness-checklist.md) references this DoD.

## Definition of Done Checklist

### Code & Implementation
- [ ] Code written and peer-reviewed (at least one approval on the PR)
- [ ] PR linked to the corresponding issue/backlog item
- [ ] No unresolved review comments
- [ ] All automated CI checks pass (unit tests, linting, security scan)

### Testing
- [ ] Unit tests written for all new logic (coverage threshold met)
- [ ] Integration tests updated or added where applicable
- [ ] End-to-end / smoke tests pass for critical flows
- [ ] Manual QA completed for features with UI or complex workflows
- [ ] No known critical or high-severity bugs outstanding

### Acceptance Criteria
- [ ] All acceptance criteria stated in the issue/backlog item are met
- [ ] Product Lead / PdM has verified acceptance criteria are satisfied
- [ ] Edge cases and error paths are handled and tested

### Documentation
- [ ] Inline code comments updated for non-obvious logic
- [ ] User-facing docs, API docs, or runbook updated if behaviour changed
- [ ] Release notes entry drafted (see [Release & Deployment Guide](octoacme-release-and-deployment.md))

### Observability
- [ ] Relevant logging, metrics, or alerts added/updated
- [ ] Feature flag or rollout strategy documented (if applicable)

### Merging
- [ ] Branch merged into the agreed integration branch
- [ ] No new merge conflicts introduced
- [ ] Feature branch deleted after merge

---

## Acceptance Criteria Format

Use the following consistent format for writing acceptance criteria in backlog items. Either **Gherkin-style** or **bullet rules** are acceptable; pick one and apply it consistently within a sprint.

### Option A — Gherkin-style (recommended for user-facing features)
```
Given <initial context>
When  <action or event>
Then  <expected outcome>
```

**Example:**
```
Given a registered user is on the login page
When  they submit valid credentials
Then  they are redirected to the dashboard and see a welcome message
```

### Option B — Bullet rules (recommended for technical/infra tasks)
```
- [ ] <Condition or behaviour that must be true>
- [ ] <Another condition>
```

**Example:**
```
- [ ] API returns HTTP 200 with a JSON body for valid input
- [ ] API returns HTTP 422 with an error message for missing required fields
- [ ] Response time < 300 ms at p95 under normal load
```

---

## Related Documents
- [Project Planning](octoacme-project-planning.md) — backlog and sprint planning reference the DoD
- [Execution & Tracking](octoacme-execution-and-tracking.md) — board workflow enforces the DoD at the **Done** column
- [Release Readiness Checklist](octoacme-release-readiness-checklist.md) — release gate references this DoD
- [RAID Log](octoacme-raid-log.md) — unresolved risks or dependencies may block DoD completion
