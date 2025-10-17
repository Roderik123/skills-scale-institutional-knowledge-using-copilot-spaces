# OctoAcme — Execution & Tracking

**Updated:** Added references to QA Lead, Release Manager, Technical Writer; linked to new QA and Release checklist documents

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
- Unit tests for new logic (owned by [Developers](octoacme-roles-and-personas.md#developers))
- Integration tests where applicable (owned by [Developers](octoacme-roles-and-personas.md#developers))
- End-to-end smoke tests for critical flows before release (coordinated by [QA Lead](octoacme-roles-and-personas.md#qa-lead))
- Security scanning in CI
- Manual QA for feature acceptance when needed (executed by [QA Lead](octoacme-roles-and-personas.md#qa-lead))

For detailed QA processes, test types, and signoff criteria, see [OctoAcme QA & Testing Guide](octoacme-qa-and-testing.md).

## Reporting & Metrics
- Track velocity and burndown
- Monitor success metrics identified in the Project One-pager
- Use dashboards for key signals (errors, latency, usage)

## Blocker Escalation
- Level 1: Team-level triage in daily standup ([Developers](octoacme-roles-and-personas.md#developers), [QA Lead](octoacme-roles-and-personas.md#qa-lead))
- Level 2: [Project Manager](octoacme-roles-and-personas.md#project-managers) escalates to [Product Manager](octoacme-roles-and-personas.md#product-managers) and dependent teams
- Level 3: Sponsor-level escalation for business-impacting issues (coordinated by [Project Manager](octoacme-roles-and-personas.md#project-managers))

For release-specific blockers, see [Release Readiness Checklist](octoacme-release-checklist.md).

## Execution Checklist
- [ ] Branching and PR conventions documented in repo
- [ ] CI configured for tests and lint
- [ ] Regular demos scheduled
- [ ] Risk register updated weekly
