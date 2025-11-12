# OctoAcme — Execution & Tracking

## Purpose
Guidance for managing day-to-day execution and tracking progress toward project milestones.

## Team Rhythm
- Daily standups (15 min) — focus on progress, blockers, dependencies
- Weekly delivery sync — show progress, updates, and flagged risks
- Demo/Review at the end of each sprint or milestone

## Workflows
- Use the project board (e.g., GitHub Projects) with columns: Backlog, Ready, In Progress, In Review, QA, Done
- Pull Request workflow:
  - Small PRs (<= 400 lines when possible)
  - Include issue link and acceptance criteria in PR description
  - Run automated tests and linting in CI before requesting review
  - Require at least one approval before merging (or team-defined policy)

## Quality & Testing
- Unit tests for new logic (owned by **Developers**)
- Integration tests where applicable (coordinated by **QA** and **Developers**)
- End-to-end smoke tests for critical flows before release (executed by **QA**)
- Security scanning in CI (managed by **DevOps Engineers**)
- Manual QA for feature acceptance when needed (performed by **QA**)

CI/CD pipeline management and test automation infrastructure is maintained by **DevOps Engineers**.

## Reporting & Metrics
- Track velocity and burndown
- Monitor success metrics identified in the Project One-pager
- Use dashboards for key signals (errors, latency, usage)

## Blocker Escalation
- Level 1: Team-level triage in daily standup (facilitated by **Scrum Master** if available)
- Level 2: **PM** escalates to Product Lead and dependent teams
- Level 3: Sponsor-level escalation for business-impacting issues

For more details on role responsibilities in execution, see [Roles and Personas](octoacme-roles-and-personas.md).

## Execution Checklist
- [ ] Branching and PR conventions documented in repo
- [ ] CI configured for tests and lint
- [ ] Regular demos scheduled
- [ ] Risk register updated weekly
