# Product Security Responsibility Matrix

- Organization / scope:
- Version / date:
- Author / reviewers:
- Status: Proposed; roles and delegated powers require confirmation
- Source of role definitions and approval:
- Review trigger: material organizational, product or risk-policy change

## How to use this matrix

For each discrete activity, identify **R** (does the work), **A** (owns completion of the activity), **C** (provides substantive input) and **I** (receives an update). Aim for one accountable function per activity and split broad activities when there are different owners. Use actual organizational functions, then map them to named people. One person can perform multiple roles. Blank cells indicate unresolved allocation, not absence of responsibility.

RACI tracks work ownership. It does **not** by itself grant a power to block a release, waive a requirement, sign a contract or accept business risk. Record those in [decision rights](product-security-decision-rights.md).

## Responsibility matrix

| Activity / work product | Responsible (R) | Accountable (A) | Consulted (C) | Informed (I) | Evidence / deliverable | Appointment gap |
|---|---|---|---|---|---|---|
| Define allowed business transactions and limits | | | | | Approved policy / requirements | |
| Prioritize a feature and security requirements | | | | | Backlog / acceptance criteria | |
| Develop design and service-level controls | | | | | Architecture and implementation | |
| Advise on abuse cases and design threats | | | | | Review with findings | |
| Maintain shared security engineering patterns | | | | | Owner, support and version record | |
| Administer corporate identity / devices | | | | | Configuration and ownership record | |
| Provide product-relevant telemetry and incident handoff | | | | | Telemetry contract / response path | |
| Operate risk register and evidence workflow | | | | | Risk records and review log | |
| Analyze severity and residual exposure | | | | | Scoped assessment and uncertainty | |
| Fix, test and verify a vulnerability | | | | | Fix and retest evidence | |
| Decide a release under approved criteria | | | | | Recorded release decision | |
| Decide residual business-risk acceptance | | | | | Authorized exception record | |
| Review unresolved exceptions and dates | | | | | Updated risk treatment record | |

## Capability boundaries to confirm

- Product Security: specialized guidance, adversarial perspective, verification and independent risk assessment.
- Engineering: secure design, implementation, remediation and operation of owned software.
- Product: requirements, acceptance criteria and roadmap priorities.
- Business owner: legitimate business rules and outcomes.
- Corporate Security: corporate identity and devices.
- Security Platform: detection and incident response, plus shared security platform services.
- Security GRC: engineering-oriented risk, governance and evidence workflows.
- CISO / security executive: standards, independence and material-risk escalation.
- Authorized risk owner: acceptance of residual risk within a documented delegation.

Do not infer a new department or headcount from each function listed.

## Outstanding decisions

| Disputed or missing assignment | Proposed resolution | Who must decide | Deadline / event trigger | Status |
|---|---|---|---|---|
| | | | | |

Use Reported, Documented, Observed, Tested, Proposed or Unknown labels for material claims. Use Scenario fact for explicitly supplied fictional premises. Do not treat a role named in a draft as an accepted appointment.
