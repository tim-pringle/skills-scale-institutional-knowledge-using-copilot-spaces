# OctoAcme Project Management Docs

Scale institutional knowledge using Copilot Spaces. This repository provides self-paced exercises and collaborative documentation for project/process management in OctoAcme.

## Overview

OctoAcme's project management approach follows a lightweight, end-to-end lifecycle that emphasizes iterative delivery, clear ownership, and measurable outcomes. Projects move through **Initiation → Planning → Execution → Release → Close/Retrospective**, with each phase supported by concrete artifacts — a **Project One-pager/Charter**, a prioritized backlog, acceptance criteria and Definition of Done, a **RAID log**, a **Decision Log**, and retrospective action items. The intent is to align stakeholders early, break work into shippable increments, and maintain a single source of truth for status and decisions.

Roles are explicitly defined to reduce ambiguity and single-person dependency. A **Project Manager (PM)** coordinates delivery mechanics (plans, schedules, risks, communications), while a **Product Manager (PdM)** owns outcomes (problem definition, prioritization, and success metrics). **Developers** are responsible for design and implementation quality (tests, documentation, review participation) and for surfacing technical risks; **QA/Testing** validates acceptance criteria and end-to-end readiness; and **Stakeholders** provide inputs and approvals. This role clarity supports faster planning and smoother execution, especially for cross-functional work.

Communication is structured around a consistent team rhythm and predictable stakeholder updates. Teams use standups and regular delivery syncs to surface progress, blockers, and dependencies, and track work on a project board (**Backlog → Ready → In Progress → In Review → QA → Done**). Risks, assumptions, issues, and dependencies are maintained in a **RAID log** and reviewed continuously, with explicit escalation paths (team triage first, then PM-to-leads, and sponsor escalation for business-impacting issues). Status updates follow the **Weekly Status Update Template** highlighting progress, next steps, risks/blockers, and decisions needed.

Quality assurance and release discipline are embedded throughout execution rather than treated as a final step. OctoAcme favors **small PRs** linked back to issues and acceptance criteria, and requires CI checks (unit tests, linting, security scans) before review and merge. Testing expectations include unit coverage for new logic, integration tests where applicable, and end-to-end smoke testing for critical flows before release. Releases follow a **Release Readiness Checklist** (staging verification, production deploy, post-deploy checks, and stakeholder announcements), with rollback/incident guidance and a strong expectation of **retrospectives** to convert learnings into owned, trackable improvement actions.

## Process Documentation Index

### Lifecycle Docs
Follow these docs in order as a project moves through its phases.

| Document | Phase | Description |
|---|---|---|
| [Project Management Overview](octoacme-project-management-overview.md) | All phases | High-level methodology, principles, roles, and RACI |
| [Project Initiation](octoacme-project-initiation.md) | Initiation | One-pager/charter, stakeholder alignment, kick-off, decision gate |
| [Project Planning](octoacme-project-planning.md) | Planning | Backlog, Definition of Done, milestones, RAID log, decision log |
| [Execution and Tracking](octoacme-execution-and-tracking.md) | Execution | Project board, PR workflow, CI, meeting cadence, metrics |
| [Risks and Communication](octoacme-risks-and-communication.md) | All phases | Risk management, escalation paths, communication cadence |
| [Release and Deployment](octoacme-release-and-deployment.md) | Release | Release readiness, deployment steps, post-deploy verification, rollback |
| [Retrospective and Continuous Improvement](octoacme-retrospective-and-continuous-improvement.md) | Close | Retrospective format, action item tracking, continuous improvement |
| [Roles and Personas](octoacme-roles-and-personas.md) | Reference | Defined roles: PM, PdM, Developers, QA/Testing, Stakeholders |

### Templates & Checklists
Reusable artifacts — copy, fill in, and store in your project repo.

| Template / Checklist | When to use |
|---|---|
| [Definition of Done](octoacme-definition-of-done.md) | Sprint planning and PR/QA review — criteria every backlog item must meet before closing |
| [Decision Log](octoacme-decision-log.md) | Ongoing — record key decisions with rationale as they are made |
| [RAID Log](octoacme-raid-log.md) | Planning onwards — track Risks, Assumptions, Issues, and Dependencies in one place |
| [Weekly Status Template](octoacme-weekly-status-template.md) | Weekly — standard stakeholder status update with metrics snapshot |
| [Release Readiness Checklist](octoacme-release-readiness-checklist.md) | Pre-release — go/no-go gate before every production deployment |
