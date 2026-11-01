# Secure by Design Evidence Review

- Application / workflow / version:
- Reviewer / date:
- Scope and evidence reviewed:
- Status: Provisional until evidence and decisions are reviewed

## Claim discipline

Reported = stakeholder statement. Documented = inspected policy or record. Observed = inspected implementation. Tested = reviewed test execution/result with scope and date. Proposed = recommendation. Unknown = no adequate evidence. Scenario fact = supplied fictional premise only.

A requirement, a screenshot of a setting and a test result support different conclusions. Keep test plans separate from executed results. Do not translate missing evidence automatically into a proven vulnerability.

## Review checklist

For each applicable question record a requirement ID, answer, claim label, source/date/scope and gap. Explain exclusions; a checklist completion is not assurance of completeness.

| Review question | Requirement ID | Answer / evidence label | Source, date and scope | Gap / next action / proposed owner |
|---|---|---|---|---|
| Is the business consequence and legitimate workflow explicit? | | | | |
| Are policy thresholds, roles and approvers confirmed rather than invented? | | | | |
| Are invariants enforced at the authoritative service for all relevant callers? | | | | |
| Are identity, resource access and action authority distinguished? | | | | |
| Do fresh accounts and installations start with appropriate protections? | | | | |
| Are safe failure and operational recovery behavior specified? | | | | |
| Are duplicate, concurrent and alternate-entry requests covered where relevant? | | | | |
| Are required audit events captured without unnecessary sensitive data? | | | | |
| Are approved reusable components maintained and correctly integrated? | | | | |
| Do tests cover allowed and denied behavior, changes and relevant recovery paths? | | | | |
| Are exception authority, scope and records explicit? | | | | |
| Does inherited exposure have an owner, interim measure and correction end condition? | | | | |
| Does AI-generated implementation receive verification beyond its own explanation? | | | | |

## Decision summary

State what is supported, what remains unknown and which gaps materially affect the business. Return a short prioritized action list with proposed owners and completion evidence. Record human design/release/risk decisions still required. Do not certify security or compliance from this checklist.
