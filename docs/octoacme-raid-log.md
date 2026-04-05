# OctoAcme — RAID Log

## Purpose
Provide a single, structured log to track **Risks**, **Assumptions**, **Issues**, and **Dependencies** (RAID) throughout a project. Keeping these in one place reduces the chance that a hidden assumption or unresolved dependency causes a late-stage surprise.

## When to use
- Create the RAID log during the **Project Planning** phase.
- Update it continuously throughout **Execution**.
- Review it at every weekly sync and before any release gate.
- Archive or close entries at project close/retrospective.

## Who owns the RAID log
The **PM** owns the overall RAID log. Individual items have named owners responsible for monitoring and resolving them.

---

## RAID Log Table

Maintain one table per category, or combine into a single table with a **Type** column — whichever suits your team.

### Risks

| ID | Description | Impact (H/M/L) | Likelihood (H/M/L) | Owner | Mitigation / Contingency | Status | Last Updated |
|---|---|---|---|---|---|---|---|
| R-001 | _Example: Third-party API may change without notice_ | H | M | Tech Lead | Pin API version; monitor changelog | Open | YYYY-MM-DD |

**Status values:** Open · Mitigated · Closed · Escalated

---

### Assumptions

| ID | Description | Owner | Validation Method | Validated? | Last Updated |
|---|---|---|---|---|---|
| A-001 | _Example: Staging environment matches production configuration_ | DevOps Lead | Review infra manifests | No | YYYY-MM-DD |

**Notes:** When an assumption is validated it may become a fact (close it) or reveal a risk/issue if it proves false (create a linked Risk or Issue entry).

---

### Issues

| ID | Description | Impact (H/M/L) | Owner | Resolution / Action | Status | Last Updated |
|---|---|---|---|---|---|---|
| I-001 | _Example: Shared test database causes flaky CI builds_ | M | Tech Lead | Introduce per-branch test databases | In Progress | YYYY-MM-DD |

**Status values:** Open · In Progress · Resolved · Deferred

---

### Dependencies

| ID | Description | Type | Dependent Team / System | Due Date | Owner | Status | Last Updated |
|---|---|---|---|---|---|---|---|
| D-001 | _Example: Auth service must expose new token endpoint before login flow can be built_ | External | Identity Team | YYYY-MM-DD | PM | Pending | YYYY-MM-DD |

**Type values:** Internal (same team) · External (another team) · Third-party · Regulatory

---

## Review Cadence

| Meeting | RAID activity |
|---|---|
| Weekly sync | Review open Risks and Issues; update status; flag escalations |
| Sprint planning | Confirm no blocking Dependencies before pulling items into sprint |
| Release gate | Confirm all High-impact Risks are Mitigated; no open High-impact Issues |
| Retrospective | Close resolved items; capture lessons learned |

---

## Escalation
- **High-impact + High-likelihood Risks** escalate to PM → Product Lead → Sponsor (see [Risks & Communication](octoacme-risks-and-communication.md)).
- **Blocking Dependencies** that cannot be resolved at team level are escalated to PM within 24 hours.

---

## Related Documents
- [Project Planning](octoacme-project-planning.md) — initial RAID log created here
- [Risks & Communication](octoacme-risks-and-communication.md) — escalation paths and stakeholder communication
- [Decision Log](octoacme-decision-log.md) — validated assumptions may generate decision entries
- [Release Readiness Checklist](octoacme-release-readiness-checklist.md) — RAID status checked at release gate
