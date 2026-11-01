# Boerum Hill Spice Company: Proposed Organization and Release-Risk Review

**Fictional planning example only.** All company details and trial results described below are Scenario facts, not verified real-world evidence. Design choices are Proposed unless otherwise stated. No real appointments, releases, accepted risks, reviews, controls or tests have occurred.

## Business and culture

Boerum Hill sells spices primarily through Shopify, has stores in New York and Paris, remote developers, a Brooklyn fulfillment warehouse, an ERP and shipping integrations. A proposed online-ordering enhancement may reduce checkout friction. In this hypothetical, an initial trial **suggests 15% more completed orders**; the sample, methodology, statistical confidence and sustained impact are Unknown.

Desired culture: engineers bring Product Security into design early to solve problems together. Engineering considers security alongside reliability and performance. Product includes risk treatment in planning. Executives support sound judgment instead of rewarding delivery speed alone. Actual culture, incentives and reporting structure are Unknown.

## Provisional roles and engagement

| Function | Proposed contribution | Status / gap |
|---|---|---|
| Commerce / Product | Own feature priority and evidence of conversion benefit | Proposed; no appointment |
| Engineering | Design and operate checkout change; evaluate workarounds and patch | Proposed; no appointment |
| Product Security | Evaluate exploit path, available mitigations and residual risk; advise independently | Proposed; no appointment |
| Business commerce executive | Weigh business consequences; accept residual risk only if delegated and permissible | Decision power Unknown |
| CISO / security executive | Own security direction, independent escalation of a disputed risk assessment | Reporting relationship Unknown |
| Corporate Security | Advise on applicable staff identity and managed-device dependencies | Scope Unknown |
| Security Platform | Coordinate necessary detection telemetry and incident response | Operational design Unknown |
| Security GRC | Maintain exception evidence, due date and review workflow if approved | Workflow Unknown |

The roles can be combined at startup scale. They do not imply eight funded teams. Use [organization design](../../templates/product-security-organization-design.md) and [RACI template](../../templates/product-security-responsibility-matrix.md) to confirm actual accountability.

## New ordering feature and contested release

**Scenario fact:** The company discovers a possible cross-site scripting issue in a third-party checkout component during review. A vendor patch is expected in weeks. Neither a CVE, proven exploit path, production exposure nor reliable patch date is supplied. XSS can have material consequences depending on context; no severity rating is inferred.

**Proposed review:** Engineering should examine whether vulnerable code is reachable, where customer data and sessions could be affected, whether the feature can exclude the component, what interim restrictions and monitoring are feasible and whether rollback is reliable. Product should substantiate the trial benefit and consider options such as staged release, redesign or waiting. Product Security should assess exploitability and consequence, record gaps and recommend a treatment. Security Platform and other functions should be consulted where controls depend on them.

**Authority:** No release or risk acceptance is approved here. The designated release owner and delegated business risk owner are Unknown. A recommendation to ship is only possible after credible review; executive acceptance cannot waive non-discretionary obligations. If an exception is approved, it must record scope, owner, reason, effective restrictions, patch plan, expiry, review triggers and independent Security dissent, if any. [Decision-rights template](../../templates/product-security-decision-rights.md).

## Illustrative decision alternatives

| Option | Potential benefit | Required evidence / unresolved exposure | Status |
|---|---|---|---|
| Defer until corrected and tested | Avoid known release exposure | Validate patch and regression effects | Proposed |
| Redesign to avoid vulnerable component | Preserve some delivery value | Verify new design avoids exploit path | Proposed |
| Limited rollout with interim mitigations | Possibly capture some benefit | Demonstrate controls, residual exposure, rollback and valid acceptance power | Proposed |

No option is selected. The risk register is not a substitute for remediation.

## Phased capability priorities

1. **First:** Confirm critical product owners, Security consultation path, actual decision delegations and exception review.
2. **Then:** Fund engineering ownership of supported design patterns, time for early review and vulnerability correction.
3. **As demand warrants:** Add dedicated product security expertise, security champions, specialist external reviews and better automation, evaluating actual backlog and exposure before headcount proposals.

See [capability roadmap](../../templates/product-security-capability-roadmap.md). All timing, resources and appointments remain Proposed or Unknown.

## Evidence needed

- Experimental design behind the 15% checkout claim.
- Component version, affected paths, vendor advisory and actual patch conditions.
- Reproduction/verification results in an authorized test environment.
- Implemented mitigation evidence and effective rollback tests.
- Actual delegated release, escalation and risk-acceptance policy.
- Identified Engineering owner, Product owner and exception-review owner.
