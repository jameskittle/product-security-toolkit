# Fictional Spice Company: Business and Product Profile

- Version: 0.1.0, October 31, 2026
- Status: Illustrative discovery record; no real assessment performed
- Record owner and reviewer: Unknown; assign before operational use
- Evidence key: **Scenario fact** means supplied fictional premise. **Assumption** is a proposed detail. **Unknown** means information was not supplied. No controls have been observed or tested.

## Business value

**Scenario fact:** A cool, fast-growing mail-order spice startup sells primarily online through Shopify. Its headquarters are in Manhattan's Flatiron District. Stores operate in NYC and Paris. A Brooklyn warehouse fulfills orders and remote developers support its digital systems. A co-packer blends spices and packages finished products; Brooklyn packs customer shipments.

Customers depend on correct orders, reliable delivery and appropriate handling of their information. Revenue, margins and operating volumes are **Unknown**.

## Essential systems

| System | Role / record ownership | Accountability | Evidence |
|---|---|---|---|
| Shopify | Storefront, customer accounts and orders; order record | Merchant configuration and integration owners unassigned; provider boundary needs documentation | Scenario fact |
| Retail POS | NYC and Paris sales; store inventory updates | Retail and technical owners unknown | Assumption: Shopify POS |
| ERP | Purchasing, suppliers, costs and financial records | Finance/operations roles proposed; actual owners unknown | Scenario fact; vendor unknown |
| Warehouse and shipping software | Picking, packing, shipment execution and carrier information | Warehouse lead and technical owner to assign | Scenario fact; vendor unknown |
| Co-packer records | Finished-product batches and lots | Supplier contact and company reconciliation owner unknown | Scenario fact |
| Custom code and integrations | Connect commerce, fulfillment and internal services | Remote developers exist; application owners and maintainers unknown | Scenario fact |
| Source and delivery systems | Change and deployment | Owner, platform and access controls unknown | Shared repository and CI/CD are working assumptions |

Inventory master, reconciliation direction and API permissions are **Unknown**. A system of record is not a substitute for a named accountable owner.

## Critical workflows

| Workflow | Identities / data | Business consequence | Owner / evidence gaps |
|---|---|---|---|
| Place an order and retrieve history | Customer identity, order and address | Cross-customer disclosure or incorrect order | Scenario fact; authorization evidence and owners unknown |
| Fulfill and ship | Integration, warehouse staff and carrier; order and shipment data | Lost orders, misdelivery or data exposure | Scenario fact; credential scope and reconciliation unknown |
| Support and refunds | Support user; customer order and refund action | Fraudulent refund or unauthorized record access | Assumption: support workflow; permission enforcement unknown |
| Reconcile retail and online stock | POS and integration identities; inventory | Overselling or inaccurate stock | Scenario fact: retail and online channels; synchronization design unknown |
| Trace lots | Co-packer and warehouse records | Inability to identify affected shipments | Scenario fact: batch/lot records; linkage to orders unverified |
| Deploy a change | Developer and deployment identity; code and configuration | Malicious or defective change reaching customers | Remote developers are Scenario fact; deployment workflow unknown |
| Introduce AI support prototype | Business builder and proposed service identity; customer orders | Excessive access or unsupported dependency | Future scenario proposal only; no deployed tool asserted |

## Candidate protect surfaces

Customer/order information; refund authority; integration credentials; deployment capability; fulfillment and inventory integrity; batch/lot records. Trace each permission across the workflow. A valid login does not establish permission to every order or privileged action.

## Obligations to verify

Payment-security responsibilities, customer privacy and cross-border data handling need review based on actual payment flows, contracts and data processing. Named reviewers are **Unknown**. Do not assert PCI DSS scope, GDPR compliance or HIPAA applicability from this profile. HIPAA is reserved for a separate healthcare example in the series.

## Priority actions

| Priority / reason | Action | Proposed owner | Completion condition |
|---|---|---|---|
| First: access can expose orders or move money | Identify application/integration owners and inventory privileged actions | Security lead with business and Engineering leads | Reviewed ownership and permission inventory |
| First: a compromised change can affect customers | Document deployment path and privileged identities | Engineering lead | Evidence-backed workflow with owner and access gaps |
| Next: disrupted handoffs affect delivery | Map order, shipment, inventory and lot reconciliation | Operations lead | Confirmed record ownership and failure-handling gaps |
| Before live AI access | Define prototype owner, data scope and support transition | Support and Engineering leads | Reviewed intake and release decision |

These priorities are consequence-based judgments, not scored findings. Actual control state is unknown.

## Questions for the next discovery round

1. Who owns each production application and integration, including after a developer leaves?
2. Which identities can export customer data, issue refunds or change integration permissions?
3. How does code reach production and what evidence exists for access and review controls?
4. Which system is the inventory master and how are failed handoffs and lot records reconciled?
5. What contracts and payment/data flows determine assurance obligations?
