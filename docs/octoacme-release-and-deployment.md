# OctoAcme — Release & Deployment Guide

**Updated:** Added references to Release Manager, QA Lead, Technical Writer; linked to Release Checklist document

## Purpose
Standardize how OctoAcme releases features to production to reduce risk and improve observability.

## Release Types
- Patch: hotfixes addressing critical production issues
- Minor: incremental features and improvements
- Major: significant functionality or breaking changes

## Pre-release requirements
- All acceptance criteria met and PRs merged ([Developers](octoacme-roles-and-personas.md#developers))
- Passing CI and security scans ([Developers](octoacme-roles-and-personas.md#developers))
- QA signoff obtained ([QA Lead](octoacme-roles-and-personas.md#qa-lead))
- UX signoff obtained for UI changes ([UX Designer](octoacme-roles-and-personas.md#ux-designer))
- Release notes drafted ([Technical Writer](octoacme-roles-and-personas.md#technical-writer))
- Documentation updated ([Technical Writer](octoacme-roles-and-personas.md#technical-writer))
- Rollback / mitigation plan documented ([Release Manager](octoacme-roles-and-personas.md#release-manager))
- Smoke tests prepared and validated ([QA Lead](octoacme-roles-and-personas.md#qa-lead))

For a complete pre-release checklist, see [Release Readiness Checklist](octoacme-release-checklist.md).

## Deployment Checklist
- [ ] Deployment window scheduled (if needed) — [Release Manager](octoacme-roles-and-personas.md#release-manager)
- [ ] Backup or snapshot (if applicable) — [Release Manager](octoacme-roles-and-personas.md#release-manager)
- [ ] Deploy to staging and run smoke tests — [Release Manager](octoacme-roles-and-personas.md#release-manager), [QA Lead](octoacme-roles-and-personas.md#qa-lead)
- [ ] Deploy to production (automated pipeline preferred) — [Release Manager](octoacme-roles-and-personas.md#release-manager)
- [ ] Run post-deploy verifications — [QA Lead](octoacme-roles-and-personas.md#qa-lead), [On-call/Support Lead](octoacme-roles-and-personas.md#on-callsupport-lead)
- [ ] Announce release to stakeholders and support — [Release Manager](octoacme-roles-and-personas.md#release-manager), [Product Manager](octoacme-roles-and-personas.md#product-managers)

For a detailed, actionable release checklist with acceptance criteria, see [Release Readiness Checklist](octoacme-release-checklist.md).

## Rollback & Incident Playbook
- If a deployment fails or causes a critical issue:
  - Trigger incident response and notify [On-call/Support Lead](octoacme-roles-and-personas.md#on-callsupport-lead)
  - [Release Manager](octoacme-roles-and-personas.md#release-manager) executes rollback to last known-good release if necessary
  - [QA Lead](octoacme-roles-and-personas.md#qa-lead) validates post-rollback smoke tests
  - Team triages root cause and captures action items

For detailed rollback procedure, see [Release Readiness Checklist - Emergency Rollback](octoacme-release-checklist.md#emergency-rollback-procedure).

## Release Notes Template
- Release name / number:
- Date:
- Summary:
- Notable changes:
- Migration steps (if any):
- Known issues:
