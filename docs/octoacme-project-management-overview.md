# OctoAcme Project Management Overview

## Purpose
Provide a concise, shareable introduction to how OctoAcme runs projects so new teammates can quickly understand our approach, roles, and key artifacts.

## Scope
Applies to all cross-functional projects that deliver product features, services, or integrations.

## Principles
- Customer-first: prioritize customer value and usability.
- Iterative delivery: deliver small, testable increments.
- Clear ownership: each project has a named Project Manager (PM) and Product Lead.
- Data-informed decisions: measure impact and iterate based on evidence.
- Psychological safety: encourage feedback and learning.

## Core Roles
- Project Manager (PM): coordinates delivery, schedules, risk, communications.
- Product Manager (PdM): defines outcomes, prioritizes backlog, and measures success.
- Developers: implement features, collaborate on design and testability.
- QA/Testing: validate quality and acceptance criteria.
- Stakeholders: provide inputs and approvals.

## Key Artifacts
- Project Charter / One-pager
- Roadmap and Release Plan
- Sprint/Iteration Backlog
- [Acceptance Criteria & Definition of Done](octoacme-definition-of-done.md)
- [RAID Log](octoacme-raid-log.md) (Risks, Assumptions, Issues, Dependencies)
- [Decision Log](octoacme-decision-log.md)
- [Weekly Status Update](octoacme-weekly-status-template.md)
- [Release Readiness Checklist](octoacme-release-readiness-checklist.md)
- Retrospective notes and action items

## Lifecycle (high-level)
1. Initiation: problem statement, stakeholders, high-level timeline.
2. Planning: scope, resources, milestones, dependencies.
3. Execution: build, test, review, iterate.
4. Release: deploy, verify, announce.
5. Close & Retrospective: capture learnings and next steps.

## Communication Cadence
- Weekly sync between PM + PdM
- Twice-weekly standups for delivery team (or as agreed)
- Monthly stakeholder updates
- Ad-hoc escalations as needed

For meeting inputs/outputs see [Execution & Tracking](octoacme-execution-and-tracking.md).

## Artifact Ownership (RACI)

**R** = Responsible (does the work) · **A** = Accountable (final sign-off) · **C** = Consulted · **I** = Informed

| Artifact | PM | PdM | Tech Lead | Developer | QA | Stakeholder |
|---|---|---|---|---|---|---|
| Project One-pager / Charter | R/A | C | C | I | I | A |
| Prioritized Backlog | C | R/A | C | C | C | I |
| RAID Log | R/A | C | C | C | I | I |
| Decision Log | R | C | R | C | I | I |
| Definition of Done | R/A | C | C | C | C | I |
| Release Notes | R | C | C | I | I | A |
| Weekly Status Update | R/A | C | C | I | I | I |
| Retrospective Action Items | R/A | C | C | C | C | I |

## How to use these docs
- Keep the Project Charter updated in the project repo.
- Add process-specific docs into `.copilot/` if you want Copilot Spaces to use them as context.
- See [docs/README.md](README.md) for the full index of lifecycle docs and templates.
