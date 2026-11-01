# Product Security Decision Rights and Risk-Acceptance Record

- Organization / system / workflow:
- Version / date:
- Status: Proposed until decision authorities confirm
- Approved decision policy or delegation source:
- Product and technical owners:
- CISO / independent security escalation:
- Legal, privacy, financial or other constraints to verify:

## Decision-authority register

| Decision | Recommends / evaluates | Decides within delegated authority | Escalation / conflicting incentives | Evidence / decision record | Authority confirmed? |
|---|---|---|---|---|---|
| Approve business rule (e.g., refund limit) | Business function, Product, Security | Designated business process owner | Executive with policy authority | Approved rule and effective date | Unknown |
| Prioritize feature and remediation work | Product, Engineering, Security | Designated product / engineering leaders within budget | Business sponsor / executive | Backlog and funding decision | Unknown |
| Assess technical exposure and mitigations | Engineering, Product Security | Authorized reviewer signs technical assessment; not business acceptance | CISO or security lead | Evidence and limitations | Unknown |
| Release under normal agreed criteria | Engineering, Product, Security | Named release owner under approved criteria | Designated executive | Release record | Unknown |
| Proceed with an exceptional known risk | Product Security advises, Engineering estimates, business owner weighs benefit | Named delegated business risk owner, where acceptance is permissible | CISO independently escalates to executive / committee | Signed, time-limited exception | Unknown |
| Change, renew or close exception | Risk owner, Engineering, Product Security, GRC | Delegated risk owner, with verified corrective evidence as applicable | CISO / governance channel | Review and closure record | Unknown |
| Respond to an active exploit / incident | Engineering, Security Platform, Product Security | Incident commander and operational owners under approved incident plan | Executive incident authority | Incident decisions and timeline | Unknown |

There is no assumed universal security veto or automatic permission to ship. If a company has an approved stop-ship authority, safety rule or emergency control, record it accurately. A business may not waive legal, regulatory, contractual or other non-discretionary requirements simply by accepting risk.

## Decision record for a specific risk

- ID / date / affected product and release:
- Proposed decision: release, defer, change scope or alternative:
- Business benefit, source and uncertainty (e.g., measured conversion impact):
- Vulnerability or threat and relevant preconditions:
- Customer, financial, operational and data impact:
- Exploitability, reachable attack paths and compensating controls:
- Evidence available, conflicting findings and what remains Unknown:
- Vendor fix expectation: source, uncertainty and contingency if delayed:
- Security recommendation and dissent, if any:
- Engineering remediation estimate / resource commitment:
- Business owner and delegation / actual authorization evidence:
- Legal / privacy / compliance review or unresolved constraint:
- Decision, rationale and timestamp:
- Scope / environment / affected customer population:
- Interim controls, monitoring and triggers to reassess or roll back:
- Remediation action, owner, due date and verification criteria:
- Exception expiration / next review:
- Risk-register reference and linked findings:
- Closure or renewal evidence and approval:

**Do not populate a pending field with an invented name, date, approval, compensating control or numerical risk score.** A planned fix is not a verified fix. An expected vendor patch is not a guaranteed arrival. A register entry preserves accountability; it does not itself mitigate exploitation.

## Independent challenge and escalation

Describe how Security's assessment reaches an executive outside the delivery chain when commercial incentives conflict. Confirm who can dispute the treatment, who decides in the organization and how dissent is preserved. Keep Security a partner in solution design.

## Evidence labels

- Scenario fact: explicitly supplied fictional premise.
- Reported: stakeholder claim or estimate, not verified.
- Documented: inspected policy or decision record.
- Observed: inspected implementation or artifact, with scope.
- Tested: reviewed executed test and results, date and scope.
- Proposed: option or recommended treatment awaiting approval.
- Unknown: evidence or decision absent.

Keep the labels attached to individual claims, not to an entire record indiscriminately.
