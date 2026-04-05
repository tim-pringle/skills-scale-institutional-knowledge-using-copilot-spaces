# OctoAcme — Decision Log

## Purpose
Capture key decisions made during a project so that the rationale is preserved, reversals are made consciously, and new team members can understand why things were built the way they were.

## When to use
Record an entry whenever a decision:
- Affects scope, architecture, tooling, or process
- Involves a trade-off with meaningful consequences
- Is likely to be questioned later or needs stakeholder visibility
- Reverses or supersedes a prior decision

## Who records decisions
| Role | Responsibility |
|---|---|
| **PM** | Records process, scope, and timeline decisions |
| **PdM** | Records product direction and prioritisation decisions |
| **Tech Lead / Developer** | Records architecture and tooling decisions |
| **Anyone** | Can raise a decision for logging; the facilitator of the relevant meeting confirms and records it |

Decisions should be logged **within 24 hours** of being made, either during or immediately after the meeting or async thread where the decision occurred.

---

## Decision Log Template

Copy the block below for each new decision entry. Store this log in the project repo (e.g., `docs/decisions/` or directly in this file) and reference it from the Project One-pager.

```markdown
### Decision [ID] — [Short title]

| Field | Detail |
|---|---|
| **Date** | YYYY-MM-DD |
| **Status** | Proposed / Accepted / Superseded / Deprecated |
| **Decider(s)** | Name(s) or role(s) |
| **Context** | What situation or problem prompted this decision? |
| **Decision** | What was decided? Be specific. |
| **Rationale** | Why was this option chosen over alternatives? |
| **Alternatives considered** | Brief note on options that were rejected and why |
| **Consequences** | What is the expected impact? What becomes easier or harder? |
| **Links** | Related issues, PRs, ADRs, or docs |
```

---

## Example Entry

### Decision 001 — Use GitHub Projects for backlog management

| Field | Detail |
|---|---|
| **Date** | 2025-01-15 |
| **Status** | Accepted |
| **Decider(s)** | PM, Tech Lead, PdM |
| **Context** | The team needed a shared backlog tool integrated with the code repository. Three options were evaluated: Jira, Linear, and GitHub Projects. |
| **Decision** | Use GitHub Projects (v2) as the primary backlog and project board. |
| **Rationale** | Already included in the GitHub plan; reduces context-switching; natively linked to issues and PRs. |
| **Alternatives considered** | Jira — powerful but adds cost and context-switching. Linear — good UX but another tool to onboard. |
| **Consequences** | All backlog items must be GitHub Issues. Reporting is lighter-weight than Jira but sufficient for current team size. |
| **Links** | [Project Planning doc](octoacme-project-planning.md) |

---

## Superseding a Decision
When a decision is reversed or replaced:
1. Update the original entry's **Status** to `Superseded`.
2. Add a **Superseded by** field pointing to the new decision ID.
3. Create a new entry explaining the updated decision and the reason for the change.

---

## Related Documents
- [Project Initiation Guide](octoacme-project-initiation.md) — decision gate at end of initiation
- [RAID Log](octoacme-raid-log.md) — assumptions that are validated become decisions
- [Project Planning](octoacme-project-planning.md) — planning decisions are recorded here
- [Roles and Personas](octoacme-roles-and-personas.md) — responsibility for decision recording
