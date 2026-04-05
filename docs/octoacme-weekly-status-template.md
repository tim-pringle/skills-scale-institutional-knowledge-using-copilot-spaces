# OctoAcme — Weekly Status Update Template

## Purpose
Provide a consistent, reusable status-update format so stakeholders always know what to expect, and PMs spend less time formatting reports and more time resolving blockers.

## When to use
Send a weekly status update every Monday (or Friday, as agreed with stakeholders) covering the previous week's progress and the week ahead. Use the same template for every project to make it easy for stakeholders to compare across initiatives.

## Who produces it
The **PM** produces and distributes the update, incorporating inputs from the PdM (product progress), Tech Lead (technical risks/blockers), and QA lead (quality status) as needed.

---

## Weekly Status Update Template

> **Copy this block, fill in each section, and distribute via the agreed channel (email, Slack, GitHub Discussions, etc.).**

```markdown
## Weekly Status Update — [Project Name]
**Week ending:** YYYY-MM-DD
**Status:** 🟢 On Track | 🟡 At Risk | 🔴 Off Track
**PM:** [Name]

---

### Summary
_One or two sentences on overall project health and the most important thing that happened this week._

---

### Progress This Week
- [Milestone / feature]: [What was completed or progressed]
- [PR / issue closed]: [Brief description]
- [Key decision made]: [Link to Decision Log entry if applicable]

### Planned Next Week
- [Task / milestone]: [Who owns it, expected outcome]
- [Dependency to resolve]: [Owner, deadline]

---

### Risks & Blockers
| ID | Description | Impact | Owner | Action / Ask |
|---|---|---|---|---|
| R-xxx | _Brief description_ | H/M/L | [Name] | [Required action or decision] |

_If no risks or blockers, write: None this week._

---

### Metrics Snapshot
| Metric | This Week | Last Week | Target |
|---|---|---|---|
| Items completed (velocity) | | | |
| Items in progress (WIP) | | | |
| Open bugs (critical/high) | | | 0 |
| Burndown on track? | Yes / No | | Yes |

_See [Execution & Tracking](octoacme-execution-and-tracking.md) for metric definitions._

---

### Decisions Needed
_List any decisions that require stakeholder or sponsor input this week. If none, write: None._

- [ ] [Decision needed]: [Context and ask] — **Owner:** [Name] — **By:** YYYY-MM-DD

---

### Links
- Project board: [link]
- RAID Log: [link to octoacme-raid-log.md or project-specific log]
- Decision Log: [link to octoacme-decision-log.md or project-specific log]
```

---

## Status Colour Guide

| Colour | Meaning |
|---|---|
| 🟢 On Track | Project is progressing as planned; no critical blockers |
| 🟡 At Risk | One or more risks or blockers could impact timeline or scope without intervention |
| 🔴 Off Track | Project is behind plan and requires immediate stakeholder attention or re-planning |

When status is 🟡 or 🔴, include a **Recovery Plan** section with specific actions and owners.

---

## Distribution
- Send to all primary stakeholders listed in the Project One-pager.
- Archive each update in the project repo (e.g., `docs/status/YYYY-MM-DD-status.md`) for historical reference.
- Escalate 🔴 status immediately to the Product Lead and Sponsor rather than waiting for the weekly cadence.

---

## Related Documents
- [Risks & Communication](octoacme-risks-and-communication.md) — escalation paths and stakeholder communication strategy
- [Execution & Tracking](octoacme-execution-and-tracking.md) — metric definitions and project board workflow
- [RAID Log](octoacme-raid-log.md) — source of truth for risks and blockers in this template
- [Decision Log](octoacme-decision-log.md) — decisions referenced in the update
