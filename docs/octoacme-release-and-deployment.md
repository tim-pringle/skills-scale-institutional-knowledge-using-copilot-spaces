# OctoAcme — Release & Deployment Guide

## Purpose
Standardize how OctoAcme releases features to production to reduce risk and improve observability.

## Release Types
- Patch: hotfixes addressing critical production issues
- Minor: incremental features and improvements
- Major: significant functionality or breaking changes

## Pre-release requirements
Before deploying, complete the [Release Readiness Checklist](octoacme-release-readiness-checklist.md). The checklist covers:
- All acceptance criteria met and PRs merged (verified against [Definition of Done](octoacme-definition-of-done.md))
- Passing CI and security scans
- Release notes drafted (see template below)
- Rollback / mitigation plan documented with named rollback owner
- Smoke tests prepared and run on staging
- Stakeholder communications prepared

## Deployment Checklist
- [ ] [Release Readiness Checklist](octoacme-release-readiness-checklist.md) completed and signed off (Go/No-Go confirmed)
- [ ] Deployment window scheduled (if needed)
- [ ] Backup or snapshot (if applicable)
- [ ] Deploy to staging and run smoke tests
- [ ] Deploy to production (automated pipeline preferred)
- [ ] Run post-deploy verifications
- [ ] Announce release to stakeholders and support

**Next phase:** [Retrospective & Continuous Improvement →](octoacme-retrospective-and-continuous-improvement.md)

## Rollback & Incident Playbook
- If a deployment fails or causes a critical issue:
  - Trigger incident response and notify on-call
  - Rollback to last known-good release if necessary
  - Triage root cause and capture action items

## Release Notes Template
- Release name / number:
- Date:
- Summary:
- Notable changes:
- Migration steps (if any):
- Known issues:
