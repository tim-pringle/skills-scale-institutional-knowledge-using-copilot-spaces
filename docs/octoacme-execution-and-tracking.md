# OctoAcme — Execution & Tracking

## Purpose
Guidance for managing day-to-day execution and tracking progress toward project milestones.

## Team Rhythm

| Meeting | Frequency | Duration | Inputs | Outputs |
|---|---|---|---|---|
| **Standup** | Daily | 15 min | Yesterday's work, blockers, dependencies | Updated board, flagged blockers, escalations to PM |
| **Weekly Delivery Sync** | Weekly | 30–45 min | [RAID Log](octoacme-raid-log.md), project board, [Weekly Status](octoacme-weekly-status-template.md) draft | Published status update, updated RAID log, decisions recorded |
| **Sprint / Demo Review** | End of sprint | 30–60 min | Completed work, acceptance criteria, DoD checklist | Stakeholder feedback, accepted/rejected items, backlog updates |
| **Retrospective** | End of sprint/release | 45–75 min | Previous action items, team sentiment | ≤3 owned action items added to backlog |

## Workflows
- Use the project board (e.g., GitHub Projects) with columns: Backlog, Ready, In Progress, In Review, QA, Done
- Pull Request workflow:
  - Small PRs (<= 400 lines when possible)
  - Include issue link and acceptance criteria in PR description
  - Run automated tests and linting in CI before requesting review
  - Require at least one approval before merging (or team-defined policy)

## Quality & Testing
- Unit tests for new logic
- Integration tests where applicable
- End-to-end smoke tests for critical flows before release
- Security scanning in CI
- Manual QA for feature acceptance when needed

## Reporting & Metrics

Use the [Weekly Status Template](octoacme-weekly-status-template.md) for stakeholder updates. Track the following metrics on the project board and dashboards:

| Metric | Definition | Where reviewed |
|---|---|---|
| **Velocity** | Number of backlog items (or story points) completed per sprint | Sprint review / weekly sync |
| **Burndown** | Remaining work vs. time left in the sprint or milestone | Daily standup / project board |
| **Cycle Time** | Time from an item moving to *In Progress* to *Done* | Weekly sync; trend over 4–6 weeks |
| **Lead Time** | Time from an item being created (backlog) to *Done* | Monthly / milestone review |
| **WIP (Work In Progress)** | Number of items currently *In Progress* (limit to reduce context-switching) | Daily standup; board column limits |
| **Open Bug Count (High/Critical)** | Number of unresolved high- or critical-severity bugs | Daily; must be 0 before release |

Monitor success metrics defined in the Project One-pager (errors, latency, usage) via dashboards.

## Blocker Escalation
- Level 1: Team-level triage in daily standup
- Level 2: PM escalates to Product Lead and dependent teams
- Level 3: Sponsor-level escalation for business-impacting issues

## Execution Checklist
- [ ] Branching and PR conventions documented in repo
- [ ] CI configured for tests and lint
- [ ] Regular demos scheduled
- [ ] [RAID Log](octoacme-raid-log.md) updated weekly
- [ ] [Weekly Status Template](octoacme-weekly-status-template.md) distributed each week
- [ ] [Definition of Done](octoacme-definition-of-done.md) visible and used during board reviews

**Next phase:** [Release & Deployment →](octoacme-release-and-deployment.md)
