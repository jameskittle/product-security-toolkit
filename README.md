# Product Security Toolkit

By James Kittle. Companion to **Building Your Business Secure by Design in the AI Age**.

Start with [Article 1: Building Your Business Secure by Design in the AI Age](https://medium.com/@jameskittle/building-your-business-secure-by-design-in-the-ai-age-e36014d4253b).

Build a product security program around your business: what creates value, which workflows matter, who owns them and what evidence supports the security decisions.

## Start here

1. Read [the discovery skill](skills/discover-business-context/SKILL.md).
2. Give your AI assistant that file and the two files in its `assets` directory. Supply a short description of your business and any approved supporting documents.
3. Ask: “Use these instructions to develop a business-context record and product profile. Identify unknowns and ask only the questions that materially change scope or priorities. Then propose a charter for review.”
4. Review the profile before asking the assistant to finish the charter. Assign real owners and confirm decision rights with those people.
5. Compare your output with the [fictional spice-company examples](examples/spice-company/product-profile.md).

For assistants that support folder-based skills, import the complete `skills/discover-business-context` folder using that assistant's documented process. Other assistants can read the same Markdown as instructions and templates. This release has been behavior-tested in this authoring environment; native import behavior on other platforms has not been tested. No credentials or integrations are required.

## Article 1 Materials

| Resource | Purpose |
|---|---|
| [Business-Context Discovery Skill](skills/discover-business-context/SKILL.md) | Guide evidence-aware discovery, prioritization and charter drafting |
| [Product Profile Template](templates/product-profile.md) | Document business purpose, workflows, data, dependencies and ownership |
| [Product Security Charter](templates/product-security-charter.md) | Establish scope, responsibilities, decision rights and measures |
| [Spice-company profile](examples/spice-company/product-profile.md) | Show a completed profile with explicit unknowns |
| [Spice-company charter](examples/spice-company/product-security-charter.md) | Show a proposed charter, with approvals still outstanding |
| [Evaluation cases](evaluations/cases.md) | Exercise the skill against incomplete and conflicting evidence |
| [Sources and attribution](docs/sources.md) | Explain the foundations and limits of the mappings |

## Article 2: Secure by Design, Secure by Default

Use the [Secure by Design Assessment Skill](skills/assess-secure-by-design/SKILL.md) with its bundled assets and your reviewed business profile.

Ask your assistant: “Assess this workflow against the five Article 2 practices. Produce explicit security requirements and an evidence review. Mark proposed rules and missing evidence, identify the authoritative service checks and suggest reusable patterns that make implementation easier. Do not run tests or change systems.”

| Resource | Purpose |
|---|---|
| [Security Requirements Register](templates/security-requirements.md) | Connect business consequences to invariants, defaults, owners and acceptance criteria |
| [Design Evidence Checklist](templates/design-evidence-checklist.md) | Separate design intent, implementation and tested effectiveness |
| [Boerum Hill Spice Company Requirements](examples/spice-company/security-requirements.md) | Follow the proposed support/refund application |
| [Boerum Hill Spice Company Evidence Review](examples/spice-company/design-evidence-review.md) | Show what can be concluded when implementation evidence is missing |
| [Assessment Evaluation Cases](evaluations/secure-by-design-cases.md) | Check ambiguous policy, approved exceptions and unsafe agent instructions |
| [Assessment Evaluation Results](evaluations/secure-by-design-results.md) | Read observed results and evaluation limits |

Import the complete assessment skill folder where supported, or provide its Markdown instructions and both assets directly to your assistant. This is an evidence-aware planning/review tool, not an automated security tester. Article 2's manuscript is in editorial preparation; no published article URL is claimed.

## Release roadmap

Version **0.2.0** adds the Article 2 assessment and requirements resources to the Article 1 toolkit. Later materials remain planned.

| Article | Companion | Status |
|---|---|---|
| 1. [Building Your Business Secure by Design in the AI Age](https://medium.com/@jameskittle/building-your-business-secure-by-design-in-the-ai-age-e36014d4253b) | Discovery skill, profile, charter and worked examples | Released |
| 2. Secure by Design, Secure by Default | Assessment skill, requirements, evidence review and examples | Toolkit available; article pending |
| 3. Applying Zero Trust to Product Architecture | Protect surfaces and Zero Trust Chains | Planned |
| 4. Building the Product Security Organization | Responsibilities and capability roadmap | Planned |
| 5. Product Security When Everyone Can Build Software | Intake and prototype transition | Planned |
| 6. Engineering Security Into Delivery | Pipeline review and release decisions | Planned |
| 7. Penetration Testing: What It Proves | Testing strategy and engagement scope | Planned |
| 8. AI and Continuous Adversarial Testing | Agent architecture and evaluation | Planned |
| 9. Outside Testers, Bug Bounties and Independent Assurance | Sourcing and research readiness | Planned |
| 10. Turning Findings Into Safer Products | Remediation and root-cause review | Planned |
| 11. Operating Product Security in Production | Readiness, telemetry and learning | Planned |
| 12. Measuring Performance and Demonstrating Assurance | Scorecard and program review | Planned |

Dates will follow the editorial schedule. See [CHANGELOG.md](CHANGELOG.md) for changes. The toolkit is available on the main branch. No GitHub Release or version tag has been created. Use commit permalinks when citing a fixed snapshot.

## Evidence and scope

An AI-written document is a proposal. A policy establishes intent; implementation evidence shows a control exists; testing provides evidence about effectiveness within its scope and date. Keep those distinctions in every output.

The toolkit uses Secure by Design and a business-first Zero Trust approach. James Kittle's **Zero Trust Chains** extends the analysis across workflows: “No decision inherits trust.” The discovery and assessment skills identify candidate boundaries and review requirements and evidence; it does not perform technical assessment, certify compliance or operate a testing agent.

Keep private business details out of public issues and examples. Use an approved AI environment and minimum necessary information. Report toolkit defects through repository issues once hosting is established; send vulnerabilities in another organization's systems through that organization's authorized disclosure channel.

## License and publication

Published at [jameskittle/product-security-toolkit](https://github.com/jameskittle/product-security-toolkit). Available under the [PolyForm Internal Use License 1.0.0](LICENSE). This source-available toolkit permits use and modification for your own internal business operations; redistribution is not permitted under this license. For other permissions, contact James Kittle through his [GitHub profile](https://github.com/jameskittle).

Copyright (c) 2026 James Kittle. Earlier revisions published under MIT remain available under their original terms. The license change begins at commit [`9b8377b`](https://github.com/jameskittle/product-security-toolkit/commit/9b8377b2803af690e4cb7435a9b47758306c662c). 

[Read Article 1 on Medium](https://medium.com/@jameskittle/building-your-business-secure-by-design-in-the-ai-age-e36014d4253b).
