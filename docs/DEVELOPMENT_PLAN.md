# FamilyHomeBoard — Development Plan

## 1. Project Overview

**Project:** FamilyHomeBoard  
**Development environment:** Windows 11 / Ubuntu WSL2  
**AI Development Agent:** OpenAI Codex  
**Cloud Platform:** Microsoft Azure  
**Methodology:** Spec-Driven Development (SDD) + Test-Driven Development (TDD)  
**Repository visibility:** Public (GitHub)  
**Languages:** Catalan (default) and English  
**Target infrastructure cost:** Maximum €2/month for initial personal use

### Project Objective

Develop an open-source, cloud-based, multi-tenant family dashboard designed for touchscreen digital photo frames and mobile devices.

The application centralizes family calendars, shopping lists, household tasks, weekly meal planning, goals, birthdays, reminders, weather information, and family photographs.

The system must support multiple independent families while maintaining strong security, privacy, low infrastructure costs, and a scalable architecture.

---

# Phase 1 — Reusable AI Engineering Environment

**Repository:** `ai-engineering-toolkit`

## Step 1 — Global Codex Configuration

**Objective:** Establish reusable development instructions and engineering standards.

### Tasks

- [ ] Verify the existing Codex CLI installation and configuration.
- [ ] Create and configure global `AGENTS.md`.
- [ ] Establish reusable project instructions.
- [ ] Define coding standards and architectural guidelines.
- [ ] Enforce SDD and TDD methodologies.
- [ ] Define secure development rules.
- [ ] Require approval before deployment or publication.
- [ ] Verify that Codex loads the global instructions.

### Deliverables

- Global `AGENTS.md`
- Reusable project templates
- Engineering standards documentation

## Step 2 — Reusable Skills

**Objective:** Create a reusable library of Codex Skills.

### Skills

- [ ] `spec-driven-development`
- [ ] `test-driven-development`
- [ ] `security-review`
- [ ] `azure-serverless`
- [ ] `code-review`

### Requirements

- Follow the official Codex Skills specification.
- Prefer trusted official sources.
- Validate each Skill before use.
- Make Skills reusable across different repositories.

### Deliverables

- Validated `SKILL.md` files
- Documentation and usage examples
- Skills discovery verification

## Step 3 — Specialized AI Agents

**Objective:** Configure independent agents for implementation review and validation.

### Agents

- [ ] **QA Reviewer:** Automated testing and TDD verification.
- [ ] **Security Reviewer:** Security audits, secrets and authorization.
- [ ] **Architecture Reviewer:** Architecture, maintainability and cloud costs.

### Requirements

- Independent reviews.
- Evidence-based validation.
- No false claims about test results.
- Security findings must be tracked and resolved.
- Verify compatibility with the installed Codex version.

### Deliverables

- Agent configurations
- Agent responsibilities
- Validation reports
- Agent execution documentation

## Step 4 — GitHub Security and DevSecOps

**Objective:** Prevent secrets and sensitive information from entering public repositories.

### Tasks

- [ ] Install and configure Gitleaks.
- [ ] Configure pre-commit security hooks.
- [ ] Create reusable GitHub Actions security workflows.
- [ ] Configure dependency vulnerability scanning.
- [ ] Scan committed Git history.
- [ ] Create secure `.gitignore` templates.
- [ ] Define `.env.example` conventions.
- [ ] Review GitHub secret scanning and push protection settings.
- [ ] Test detection using fictitious secrets.
- [ ] Require security validation before releases.

### Security Policies

- Never commit passwords, tokens or cloud credentials.
- Never expose Azure Storage keys.
- Prefer Managed Identity and OIDC.
- Never log sensitive information.
- Never disable security controls to bypass failures.
- Require explicit approval before deployment.

### Deliverables

- Git security hooks
- GitHub Actions templates
- Security scripts
- Security policy documentation

---

# Phase 2 — FamilyHomeBoard Specifications

**Repository:** `familyhomeboard`

## Step 5 — Project Initialization

**Objective:** Prepare the application repository for SDD development.

### Tasks

- [ ] Validate repository structure.
- [ ] Install and initialize GitHub Spec Kit.
- [ ] Configure project-specific `AGENTS.md`.
- [ ] Integrate reusable Skills and agent workflows.
- [ ] Configure project security checks.
- [ ] Prepare frontend, backend and infrastructure directories.
- [ ] Configure initial CI workflows.
- [ ] Establish documentation conventions.

### Deliverables

- Project structure
- Spec Kit configuration
- `AGENTS.md`
- Initial CI configuration

## Step 6 — Functional Specifications (SDD)

**Objective:** Define requirements before implementing production code.

### Features

- [ ] Family dashboard home screen
- [ ] Weekly family calendar
- [ ] Individual family member schedules
- [ ] Upcoming events and countdowns
- [ ] Shared shopping list
- [ ] Household tasks
- [ ] Family goals
- [ ] Birthdays and anniversaries
- [ ] Weekly meal planning
- [ ] Weather information
- [ ] Family reminders
- [ ] Family member management
- [ ] Settings and preferences
- [ ] Catalan and English localization
- [ ] Touchscreen and mobile responsive layouts

### Digital Photo Frame Mode

- [ ] Optional photo frame mode
- [ ] Automatic activation after 5 minutes of inactivity
- [ ] Configurable inactivity timeout
- [ ] Configurable slideshow interval
- [ ] Azure Blob Storage integration
- [ ] Private image access
- [ ] Full-screen slideshow
- [ ] Return to dashboard on touch

### Multi-Tenant Requirements

- [ ] Multiple independent families
- [ ] Family administrators
- [ ] Role-based authorization
- [ ] Users belonging to multiple families
- [ ] Device registration and revocation
- [ ] Strict family data isolation

### Deliverables

- Functional specifications
- User stories
- Acceptance criteria
- Non-functional requirements
- MVP scope definition

---

# Phase 3 — Architecture and Security Design

## Step 7 — Azure Serverless Architecture

**Objective:** Define a secure, scalable, low-cost Azure architecture.

### Proposed Technology Stack

| Component | Technology |
|---|---|
| Frontend | React + TypeScript |
| Frontend Hosting | Azure Static Web Apps |
| Backend | Azure Functions |
| Data Storage | Azure Table Storage |
| Photo Storage | Azure Blob Storage |
| Infrastructure as Code | Terraform |
| CI/CD | GitHub Actions |
| Authentication | To be finalized during architecture design |
| Identity Management | User and device identities |
| Observability | Cost-optimized Azure monitoring |

### Tasks

- [ ] Define application architecture.
- [ ] Design multi-tenant data model.
- [ ] Design user authentication.
- [ ] Design device registration and authentication.
- [ ] Define role-based authorization.
- [ ] Design private photo access.
- [ ] Define API contracts.
- [ ] Document architecture decisions (ADRs).
- [ ] Create a threat model.
- [ ] Estimate Azure monthly costs.
- [ ] Define cost monitoring and budget alerts.
- [ ] Validate compatibility with Azure free tiers.

### Cost Requirements

Target infrastructure cost: **€2/month maximum for initial personal use**.

Costs must be monitored and documented. This is an engineering target, not a guaranteed Azure billing limit.

### Deliverables

- Architecture diagrams
- API specifications
- Data model
- Security architecture
- ADRs
- Cost estimation

---

# Phase 4 — Implementation

## Step 8 — Test-Driven Development

**Objective:** Implement features using the RED → GREEN → REFACTOR process.

### Development Workflow

For each feature:

1. Review the approved specification.
2. Define acceptance criteria.
3. Write automated tests.
4. Execute tests and confirm expected failure (RED).
5. Implement minimum required functionality.
6. Execute tests and confirm success (GREEN).
7. Refactor the implementation.
8. Execute tests again.
9. Run independent QA review.
10. Run independent security review.
11. Verify CI quality gates.

### Implementation Order

- [ ] Dashboard UI with mocked data
- [ ] Navigation and touchscreen interactions
- [ ] Catalan and English localization
- [ ] Photo frame mode
- [ ] Shopping list
- [ ] Household tasks and goals
- [ ] Birthdays and anniversaries
- [ ] Weekly meal planner
- [ ] Calendar integration
- [ ] Weather integration
- [ ] Backend persistence
- [ ] User authentication
- [ ] Family and device management
- [ ] Multi-tenant authorization
- [ ] Azure Blob Storage photo integration

### Deliverables

- Working application components
- Automated tests
- QA and security review reports
- Test execution evidence

---

# Phase 5 — Validation

## Step 9 — Quality Assurance and Security

**Objective:** Validate the complete application before deployment.

### Tests

- [ ] Unit tests
- [ ] Integration tests
- [ ] End-to-end tests
- [ ] Touchscreen interaction tests
- [ ] Responsive design tests
- [ ] Internationalization tests
- [ ] Accessibility tests
- [ ] Authentication tests
- [ ] Authorization tests
- [ ] Multi-tenant isolation tests
- [ ] Device revocation tests
- [ ] Photo access security tests
- [ ] Secret scanning
- [ ] Dependency vulnerability scanning
- [ ] Infrastructure security scanning

### Mandatory Security Cases

- Family A cannot access Family B data.
- Users cannot bypass authorization by changing family identifiers.
- Unauthenticated requests cannot access private resources.
- Revoked devices cannot retrieve protected data.
- Expired or forged tokens are rejected.
- Azure credentials are never embedded in frontend bundles.
- Photo containers are not publicly accessible.
- Git repositories and history contain no detected secrets.

### Release Criteria

A release must not proceed when mandatory security or functional checks fail.

Every validation result must have supporting evidence.

### Deliverables

- Test reports
- Security audit
- Vulnerability findings
- Go / No-Go decision

---

# Phase 6 — Azure Deployment

## Step 10 — Infrastructure and Production Deployment

**Objective:** Deploy FamilyHomeBoard securely to Azure.

### Tasks

- [ ] Create Terraform infrastructure modules.
- [ ] Configure Azure Static Web Apps.
- [ ] Configure Azure Functions.
- [ ] Configure Azure Table Storage.
- [ ] Configure private Blob Storage.
- [ ] Configure identities and RBAC.
- [ ] Configure GitHub Actions with OIDC where supported.
- [ ] Configure HTTPS and secure API access.
- [ ] Configure minimal observability.
- [ ] Configure cost alerts.
- [ ] Validate infrastructure security.
- [ ] Run deployment readiness checks.
- [ ] Perform deployment with explicit approval.
- [ ] Execute production smoke tests.
- [ ] Document rollback procedures.

### Deliverables

- Terraform code
- CI/CD pipelines
- Production environment
- Security validation
- Cost monitoring
- Deployment documentation

---

# Definition of Done

A feature is complete only when:

- [ ] Specification is approved.
- [ ] Acceptance criteria are satisfied.
- [ ] Tests were written before production implementation.
- [ ] Automated tests pass.
- [ ] Security review is completed.
- [ ] Code review is completed.
- [ ] No critical or high-severity security findings remain unresolved.
- [ ] No secrets are detected in the relevant Git changes.
- [ ] Documentation is updated.
- [ ] CI quality gates pass.

# Project Status

**Current phase:** Phase 1 — Reusable AI Engineering Environment

**Repositories:** Created

**Next action:** Verify global Codex configuration and reusable Skills.

**Development policy:** No unauthorized deployment or Git push.
