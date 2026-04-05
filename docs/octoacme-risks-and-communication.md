# OctoAcme — Risk Management & Communication

## Purpose
Explain how to identify, manage, and communicate risks and dependencies.

## Risk & RAID Management

Maintain a [RAID Log](octoacme-raid-log.md) as the single source of truth for Risks, Assumptions, Issues, and Dependencies.

### Risk Register fields (within the RAID Log)
- ID, Description, Impact (H/M/L), Likelihood (H/M/L), Owner, Mitigation plan, Status

### Risk Lifecycle
- Identify: during planning and ongoing execution
- Assess: estimate impact and likelihood
- Mitigate: reduce via actions or contingency plans
- Monitor: review at weekly syncs and update status in the RAID Log

## Stakeholder Communication
- Identify stakeholder groups and communication needs (e.g., engineering, sales, support)
- Provide regular updates (weekly or milestone-based) using the [Weekly Status Template](octoacme-weekly-status-template.md)
- Use a single source of truth (project README or release doc) for status

## Communication Templates
See the dedicated template docs for copy/paste-ready formats:
- **Weekly Status Update** — [octoacme-weekly-status-template.md](octoacme-weekly-status-template.md)
- **Decision Log** — [octoacme-decision-log.md](octoacme-decision-log.md)

**Incident Communication**
- Triage summary
- Actions being taken
- Expected timeline
- Post-incident blameless retrospective scheduled

## Escalation Paths
- Team-level -> PM -> Product Lead -> Sponsor
- For security incidents, follow the security incident runbook and notify Security on-call
