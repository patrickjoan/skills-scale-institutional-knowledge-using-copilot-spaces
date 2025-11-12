# OctoAcme — Release & Deployment Guide

## Purpose
Standardize how OctoAcme releases features to production to reduce risk and improve observability.

## Release Types
- Patch: hotfixes addressing critical production issues
- Minor: incremental features and improvements
- Major: significant functionality or breaking changes

## Pre-release requirements
- All acceptance criteria met and PRs merged (validated by **QA**)
- Passing CI and security scans (verified by **DevOps Engineers**)
- Release notes drafted (prepared by **Technical Writer** with input from **PdM** and **PM**)
- Rollback / mitigation plan documented (created by **DevOps Engineers**)
- Smoke tests prepared (designed by **QA**)

**DevOps Engineers** are accountable for deployment execution. See [Roles and Personas](octoacme-roles-and-personas.md) for the full RACI matrix.

## Deployment Checklist
- [ ] Deployment window scheduled (if needed) - coordinated by **PM**
- [ ] Backup or snapshot (if applicable) - executed by **DevOps Engineers**
- [ ] Deploy to staging and run smoke tests - deployed by **DevOps**, tested by **QA**
- [ ] Deploy to production (automated pipeline preferred) - managed by **DevOps Engineers**
- [ ] Run post-deploy verifications - validated by **DevOps** and **QA**
- [ ] Announce release to stakeholders and support - communicated by **PM** to **Stakeholders** and **Support & Operations**

## Rollback & Incident Playbook
- If a deployment fails or causes a critical issue:
  - Trigger incident response and notify on-call (**DevOps Engineers** or **Support & Operations**)
  - Rollback to last known-good release if necessary (executed by **DevOps Engineers**)
  - Triage root cause and capture action items (led by **PM** with **DevOps**, **Developers**, and **QA**)
  - Post-incident blameless retrospective scheduled (facilitated by **Scrum Master** or **PM**)

## Release Notes Template
- Release name / number:
- Date:
- Summary:
- Notable changes:
- Migration steps (if any):
- Known issues:
