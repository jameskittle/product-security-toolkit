# Boerum Hill Spice Company: Proposed Refund Requirements

Version 0.2.0. Fictional worked example. No implementation inspected or tests executed.

## Context and business rules

Scenario facts: Boerum Hill Spice Company sells spices primarily online through Shopify, with NYC and Paris stores, Flatiron offices, Brooklyn fulfillment, an ERP and remote developers. Proposed feature: a support application combines orders, shipment status and refunds. Its exact service architecture is Unknown; the enforcement points below are logical design responsibilities, not assertions about Shopify APIs.

Business outcome: resolve customer issues quickly while preserving order privacy, refund integrity and investigation records. Support and Finance must confirm eligibility, per-role limits, cumulative refund rules and approval authority. No monetary threshold or approval appointment is assumed. Product, Engineering and Product Security are proposed functional owners; named assignees and staffing remain Unknown.

## Proposed invariants

| ID | Consequence | Condition / service enforcement | Default | Acceptance criteria and evidence |
|---|---|---|---|---|
| BH-01 | Unauthorized refund | Authoritative refund service verifies actor, eligible order and permitted action for every UI, API, job or agent request | Refund execution unavailable until explicitly granted | Allow a permitted case; deny missing authority and out-of-scope order through every entry path. Need implementation inspection and scoped execution results |
| BH-02 | Excessive or duplicate refund | Enforce approved cumulative limits against authoritative transaction state, including concurrent and repeated requests | No refund beyond approved rules | Retry the same operation and submit distinct concurrent requests; confirm final money movement stays within approved total. Need atomicity design and result records |
| BH-03 | Payment during unverifiable authority | If authority cannot be established, decline the refund and provide a retry/escalation path | No fail-open money movement | Simulate authorization dependency failure; verify no payment and clear recoverable status. Results Unknown |
| BH-04 | Uninvestigable action / leaked secrets | Record actor, order, applicable approval and outcome; exclude credentials and unnecessary customer data | Audit enabled; sensitive payload logging disabled | Trace an allowed and denied request; inspect log access and contents. Retention and access owners to confirm |
| BH-05 | Customer record exposure | Enforce order access and field scope for each support or integration identity | Minimum approved lookup access | Attempt unrelated-order access, bulk export and unneeded fields; confirm required work remains possible. Exact scope awaits business approval |

All criteria and controls are Proposed. None is marked Observed or Tested.

## Make implementation easier

Propose a maintained authorization component, refund transaction/idempotency pattern and structured audit mechanism. Engineering must confirm provider capabilities and integration design. Business owners supply order scope and refund policy. Component maintainers own shared behavior; application engineers own correct use. Published examples and permitted/denied test fixtures reduce repeated design and late rework.

## Exceptions, changes and existing systems

A larger refund requires a designated approver under the approved policy. This preserves BH-01 and BH-02 when the business-defined limits include the authorized approval path. Actual authority, thresholds, expiry needs and evidence remain Unknown. No release permission is granted by this example.

Regression checks: repeat BH-01 through BH-05 for a new endpoint, changed dependency or relevant restoration. These checks preserve requirements after change; they are distinct from fresh-account defaults.

If the current integration has an overbroad administrative credential, treat that as a hypothetical condition until inspected. Proposed action: confirm actual permissions, restrict use and monitor as an interim measure, then redesign for scoped identities. Proposed owner: Engineering with the business/system owner; completion: verified required access and denied unrelated actions. No existing vulnerability is asserted.
