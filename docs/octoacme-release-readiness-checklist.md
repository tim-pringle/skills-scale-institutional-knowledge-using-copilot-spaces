# OctoAcme — Release Readiness Checklist

## Purpose
Provide a structured go/no-go gate to verify that a release is safe to deploy to production. Working through this checklist before every release reduces incidents, miscommunications, and rushed rollbacks.

## When to use
Complete this checklist **before every production release** (patch, minor, or major). The PM and Tech Lead sign off jointly. For hotfixes, a compressed version of this checklist still applies — skip only items explicitly marked *(hotfix optional)*.

## Who owns it
| Role | Responsibility |
|---|---|
| **PM** | Confirms stakeholder comms, release notes, and schedule |
| **Tech Lead** | Confirms technical readiness, CI, and rollback plan |
| **QA Lead** | Confirms testing is complete and no blocking bugs remain |
| **PdM** | Confirms acceptance criteria and product sign-off |

---

## Release Readiness Checklist

### 1. Code & Quality
- [ ] All planned issues/PRs for this release are merged to the release branch
- [ ] All acceptance criteria are met (verified against [Definition of Done](octoacme-definition-of-done.md))
- [ ] No open critical or high-severity bugs linked to this release
- [ ] CI pipeline is green (unit tests, integration tests, linting, security scan)
- [ ] End-to-end smoke tests pass on the staging environment
- [ ] Dependency updates reviewed for vulnerabilities *(hotfix optional)*

### 2. Pre-production Verification
- [ ] Release branch deployed to **staging** successfully
- [ ] Smoke test suite executed on staging — all critical paths pass
- [ ] Performance / load profile reviewed if significant changes were made *(hotfix optional)*
- [ ] Data migrations (if any) tested on a staging copy of production data *(hotfix optional)*
- [ ] Feature flags configured correctly for target environments

### 3. Rollback & Incident Preparedness
- [ ] **Rollback owner** named: ________________________
- [ ] Rollback procedure documented and tested (or link to runbook): ___________
- [ ] On-call rotation confirmed for the release window
- [ ] Monitoring / alerting thresholds reviewed and active
- [ ] Incident communication channel ready (Slack/Teams bridge, etc.)

### 4. Documentation & Communications
- [ ] Release notes drafted and reviewed (see [Release & Deployment Guide](octoacme-release-and-deployment.md))
- [ ] Internal stakeholder announcement prepared (Slack, email, or release announcement)
- [ ] Customer-facing changelog or comms prepared *(if applicable)*
- [ ] Support team briefed on changes and known issues
- [ ] Runbook / ops docs updated to reflect any changed behaviour

### 5. Schedule & Logistics
- [ ] Deployment window confirmed with team and stakeholders
- [ ] Deployment pipeline / automation verified and dry-run completed *(hotfix optional)*
- [ ] Any required maintenance window communicated to affected users
- [ ] Post-deploy verification steps documented and assigned

### 6. Approval (Go/No-Go)

| Role | Name | Sign-off | Date |
|---|---|---|---|
| PM | | ☐ Go  ☐ No-Go | |
| Tech Lead | | ☐ Go  ☐ No-Go | |
| QA Lead | | ☐ Go  ☐ No-Go | |
| PdM | | ☐ Go  ☐ No-Go | |

> **Go** = all checklist items verified; ready to deploy.
> **No-Go** = one or more blocking items remain; release is postponed until resolved.

**No-Go items to resolve before re-review:**
- [ ] _Item 1_
- [ ] _Item 2_

---

## Post-Deploy Verification (complete after deployment)
- [ ] Application is up and responding (health endpoint / smoke test)
- [ ] Key user flows verified in production
- [ ] Error rates and latency are within normal baselines
- [ ] No unexpected alerts fired within 15 minutes of deployment
- [ ] Release announcement sent to stakeholders
- [ ] Retrospective / post-release review scheduled *(for major releases)*

---

## Related Documents
- [Release & Deployment Guide](octoacme-release-and-deployment.md) — deployment steps, release notes template, rollback playbook
- [Definition of Done](octoacme-definition-of-done.md) — quality criteria checked at release gate
- [RAID Log](octoacme-raid-log.md) — confirm no open High-impact risks or blocking dependencies
- [Weekly Status Template](octoacme-weekly-status-template.md) — communicate release status to stakeholders
