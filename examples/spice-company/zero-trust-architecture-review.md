# Boerum Hill Spice Company: Support Workflow Architecture Review

Version 0.3.0. Fictional design exercise supporting Article 3. No production implementation inspected and no security tests executed.

## Protect surface

Scenario facts: Boerum Hill sells spices primarily through Shopify, with NYC and Paris stores, Flatiron offices, Brooklyn fulfillment, an ERP and remote developers. A proposed support app combines order lookup, shipment status and refund requests.

Protect customer-order information and refund authority. Exposure could disclose customer information or permit unauthorized money movement. Include supporting identities, credentials and services. This is a bounded support-workflow review, not an assessment of every store, co-packer, warehouse or ERP process.

Company-controlled custom code, staff permissions and integration configuration must work within supplier capabilities. Actual provider API scopes, deployment topology and delegation support are Unknown. No Shopify vulnerability is asserted. Business, Engineering and Product Security are proposed functional owners; named assignments and policy approval remain open.

Related requirements: [BH-01 through BH-05](security-requirements.md). These remain Proposed.

## Transaction flow and proposed controls

| Step | Actor / service and operation | Required authority and enforcement | Evidence / failure behavior |
|---|---|---|---|
| Sign in | Support employee opens app | Verify employee session and applicable device conditions; login alone does not grant refund permission | Proposed; identity configuration and session controls needed |
| Retrieve order | Support service calls order capability | Authenticate workload and validate employee's permitted order/field scope at authoritative service | Proposed; unrelated-order and bulk-access checks planned |
| Check shipment | Shipment integration retrieves status | Limit identity to necessary status data; prevent access to refund/admin capability | Proposed; provider scopes and alternate access paths Unknown |
| Request refund | App submits actor, order, amount and approval context | Controlled refund service validates trustworthy actor/delegation context and policy; caller-supplied employee name is insufficient | Proposed; policy and delegation mechanism need confirmation |
| Execute refund | Controlled service invokes provider | Keep provider credential inaccessible to bypass callers; narrow supported scopes; bind approval to order and amount; enforce cumulative limits atomically | Proposed; deny unverifiable authority, prevent duplicate/excess payment and provide recovery |
| Investigate / revoke | Operators trace actions and disable access | Correlate actor, service, order, approval and outcome without secrets; define revocation effect on sessions and queued jobs | Proposed; owner, retention and accepted revocation timing Unknown |

## Architectural decision

Hypothetical risk: an employee may read orders but cannot issue refunds, while the app credential permits both. Forwarding the refund under that credential without checking the employee's authority amplifies privilege.

Propose an authoritative refund service that checks the originating authority before provider execution. Restrict credential access and all alternate invocation paths to prevent bypass. Evaluate supplier constraints before choosing the mechanism. A separate service is one possible boundary; service separation alone does not prove authorization.

Proposed decision owner: Engineering, with Support/Finance confirming policy and Product Security reviewing the design. Completion requires named ownership, approved business rules, inspected enforcement and scoped test results. No monetary limit or approver is appointed by this example.

## Verification plan and evidence gaps

| Requirement / concern | Planned check | Current evidence |
|---|---|---|
| BH-01: permission and bypass | Deny non-refund employee through UI, API, job and agent; deny forged delegation; allow authorized request | No implementation or results supplied |
| BH-02: transaction integrity | Retry one request and submit distinct concurrent requests; verify authoritative cumulative total | Business limits, atomicity and execution results Unknown |
| BH-03: safe failure | Make authority check unavailable; verify no refund and recoverable status | Plan only |
| BH-04: investigation | Trace allowed/denied actions; inspect log fields and access | Plan only; retention policy Unknown |
| BH-05: order privacy | Deny unrelated orders, excess fields and bulk extraction | Exact approved scope Unknown |
| Revocation | Revoke user/workload permission and examine sessions plus queued work | Accepted timing and results Unknown |

AI extension: decide whether an assistant advises, acts with delegated authority or has independent task authority. Enforce its data and action limits in the same services outside the model. A prompt promising to avoid refunds supplies no implementation evidence.

## Next actions

1. Support and Finance: approve eligibility, scope, limits and approval authority.
2. Engineering: inspect provider permissions, choose validated delegation and credential boundaries, document bypass prevention and retry/concurrency design.
3. Product Security: review the design and evidence against BH-01 through BH-05.
4. Operations: assign investigation and revocation responsibilities with completion criteria.

All design recommendations remain Proposed. This exercise provides no release authorization, compliance determination or production assurance.
