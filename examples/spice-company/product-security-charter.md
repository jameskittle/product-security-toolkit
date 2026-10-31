# Fictional Spice Company: Proposed Product Security Charter

- Version: 0.1.0, October 31, 2026
- Status: Proposed example; no approvals or control effectiveness asserted
- Sponsor: Executive with security accountability; actual appointment unknown
- Program lead: Designated security lead; proposed, not assigned
- Approval evidence: None

## Mission

Protect the digital capabilities that let customers discover spices, place orders and receive the correct products. Support growth while protecting customer information, transaction integrity and dependable fulfillment.

## Scope

Include the online storefront, customer services, custom applications, integrations and their source/delivery systems. Apply AppSec practices to internal tools. Coordinate ERP, warehouse and retail risks with their business and IT owners. Include co-packer data handoffs and traceability dependencies. Physical warehouse operations and food-quality decisions remain with the responsible operating functions; Product Security addresses their software and data dependencies.

Map the company's responsibilities for configuration, access, installed applications and custom code separately from provider-operated services. Confirm exact boundaries from contracts and architecture evidence.

## Principles

Prioritize business consequences. Build security requirements and safe defaults into the work. Follow protect surfaces and transaction flows. Apply James Kittle's Zero Trust Chains principle: no decision inherits trust. Distinguish intent, implementation and tested effectiveness.

## Proposed responsibilities

| Role | Responsibility | Decision boundary |
|---|---|---|
| CISO or designated security executive | Security direction, requirements, independent assessment and escalation | Escalate material exposure; appointment and delegation pending |
| Product Security lead | Discovery, guidance, review and assessment coordination | Assess and advise; no unilateral risk acceptance assumed |
| Engineering lead | Code ownership, secure implementation, maintenance and remediation | Deliver within agreed release criteria |
| Commerce / Product lead | Customer workflow requirements and prioritization | Own outcome and roadmap decisions |
| Operations lead | Fulfillment, inventory and supplier handoffs | Confirm record ownership and operating requirements |
| IT / system owners | Purchased-platform configuration and identity administration | Own assigned services and vendor handoffs |
| Authorized executive risk owner | Funding and residual-risk acceptance | Authority and monetary/exposure thresholds to approve |

All named appointments remain open. Several responsibilities may be held by the same person; no new department is assumed.

## Proposed operating commitments

Use one application/integration intake record with owner, data, permissions and maintenance responsibility. Review consequential design changes before implementation. Establish delivery checks proportionate to risk, assign verified findings and retest fixes. Define incident notification and revocation responsibilities with Engineering and IT. Reconcile failed order and inventory handoffs with Operations.

Review priorities monthly initially and revisit scope after new integrations, material access changes, AI features or incidents. This cadence is a proposal pending resource and leadership agreement.

## Release and exception decisions

Leadership must approve release criteria and identify the final escalation authority. Before live customer-data access, a prototype needs a supported owner, bounded permissions, an approved delivery path and evidence of relevant testing. An exception must state exposure, compensating measures, authorized risk owner, expiry and remediation commitment. No exception or stop-release power is granted by this example.

## Initial priorities and evidence

Use the action list in the [business profile](product-profile.md): identify privileged-access owners, document production deployment, map fulfillment/traceability handoffs and review any AI prototype before live access. Funding and actual assignees remain unknown.

Establish a baseline for critical workflows with confirmed owners and examined access decisions, unresolved material exposure and remediation completion verified by retest. Track recurrence after sufficient history exists. Avoid arbitrary targets before evidence is available.

## Approval needed

Confirm the sponsor, owners, resources, release and exception authority, scope and review cadence. Retain Proposed status until approval evidence exists.
