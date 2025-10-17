# OctoAcme — QA & Testing Guide

**Added:** QA and testing guidance for OctoAcme projects

## Purpose
Define quality assurance practices, test ownership, and QA responsibilities to ensure consistent quality across OctoAcme releases.

## Test Ownership

### Developers
- Write and maintain **unit tests** for new code
- Write **integration tests** for component interactions
- Ensure tests pass in CI before requesting PR review
- Fix failing tests and address test coverage feedback

### QA Lead
- Define test strategy and coverage requirements
- Review and approve test plans for features
- Execute or coordinate **manual acceptance testing**
- Maintain and run **end-to-end (e2e) tests** for critical user flows
- Own **smoke test** suites for release validation
- Track quality metrics and test coverage

## Types of Tests

### Unit Tests
- Test individual functions, methods, or classes in isolation
- Should be fast, deterministic, and run in CI on every commit
- Target: maintain >80% code coverage for business logic

### Integration Tests
- Test interactions between multiple components or services
- Verify API contracts, database interactions, and external dependencies
- Run in CI and should complete within reasonable time limits

### End-to-End (E2E) Tests
- Validate complete user flows from UI to backend
- Test critical paths (e.g., login, checkout, data submission)
- May run in CI for critical paths; longer suites run nightly or pre-release

### Smoke Tests
- Quick validation tests that verify core functionality after deployment
- Run immediately after deploying to staging and production
- Must complete in under 10 minutes
- Focus on: authentication, key APIs, critical user journeys, and health checks

## Test Environments

### Local Development
- Developers run unit and integration tests locally
- Use mocks or local services for dependencies

### CI Environment
- Automated tests run on every PR
- Includes unit, integration, and critical e2e tests
- Must pass before merge is allowed

### Staging Environment
- Mirror of production for pre-release testing
- Used for full e2e test suites and manual QA
- QA Lead validates acceptance criteria here

### Production Environment
- Smoke tests run post-deployment
- Monitoring and alerting validate production health
- Manual exploratory testing may occur for critical releases

## Test Signoff Criteria

Before a feature is considered "ready for release", the following must be met:

- [ ] All automated tests (unit, integration, e2e) pass in CI
- [ ] Code coverage meets or exceeds team standards (≥80% for new code)
- [ ] Manual acceptance testing completed by QA Lead (if applicable)
- [ ] No open critical or high-priority bugs
- [ ] Smoke tests pass in staging environment
- [ ] Security scans (SAST/DAST) pass with no critical vulnerabilities
- [ ] Performance tests pass (if applicable to feature)
- [ ] Accessibility requirements validated (if UI changes)

## QA Responsibilities During Release Readiness

The [QA Lead](octoacme-roles-and-personas.md#qa-lead) ensures the following during release preparation:

1. **Test Planning (early in development)**
   - Review feature specs and acceptance criteria
   - Define test cases and coverage requirements
   - Identify areas requiring manual testing

2. **During Development**
   - Monitor test coverage and CI results
   - Triage and prioritize bugs
   - Provide feedback on testability and quality issues

3. **Pre-Release Validation**
   - Execute manual test plans in staging
   - Run full e2e test suites
   - Validate acceptance criteria are met
   - Verify smoke tests are prepared and passing

4. **Release Signoff**
   - Confirm all signoff criteria are met
   - Document any known issues or limitations
   - Provide formal QA signoff to [Release Manager](octoacme-roles-and-personas.md#release-manager)

5. **Post-Release**
   - Monitor smoke tests and production health
   - Triage any post-release issues
   - Participate in retrospectives and improve test processes

## QA Checklist

Use this checklist to ensure QA readiness before release. See also [Release Checklist](octoacme-release-checklist.md) for complete release readiness.

### Pre-Development
- [ ] Test strategy defined and reviewed with team
- [ ] Acceptance criteria are clear and testable
- [ ] Test environment access and test data prepared

### During Development
- [ ] Unit test coverage ≥80% for new code
- [ ] Integration tests written for new component interactions
- [ ] CI tests passing on all PRs
- [ ] Bugs triaged and prioritized

### Pre-Release
- [ ] All automated tests passing in staging
- [ ] Manual acceptance test cases executed
- [ ] Smoke tests prepared and validated in staging
- [ ] No critical or high-priority open bugs
- [ ] Security scans completed and vulnerabilities addressed
- [ ] Performance validated (if applicable)
- [ ] Accessibility requirements met (if UI changes)
- [ ] Rollback plan reviewed and understood

### Release Signoff
- [ ] QA Lead formal signoff provided to Release Manager
- [ ] Known issues documented in release notes
- [ ] Smoke tests ready for post-deployment execution

### Post-Release
- [ ] Post-deployment smoke tests passed
- [ ] Production monitoring validated
- [ ] Any post-release issues triaged and prioritized
- [ ] QA lessons learned captured for retrospective

---

**Related Documents:**
- [OctoAcme Roles & Personas](octoacme-roles-and-personas.md)
- [OctoAcme Release Checklist](octoacme-release-checklist.md)
- [OctoAcme Execution & Tracking](octoacme-execution-and-tracking.md)
