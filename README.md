# FuturePays | PCI DSS v4.0.1 Audit-Readiness Case Study

**Jamal Davison · Cybersecurity / GRC Portfolio**

> **Fictional educational scenario.** This repository demonstrates assessment planning and documentation, not a completed PCI DSS assessment or certified payment environment. Technical validation, evidence collection, and remediation testing have not been performed.

## The challenge
FuturePays is a hypothetical e-commerce retailer using a third-party hosted payment page. Its merchant website controls checkout redirection, so scoping must consider systems that could affect payment security, not just systems that store payment card numbers.

## The approach
1. Model the proposed payment flow and trust boundaries.
2. Identify systems and mark preliminary PCI DSS scope assumptions.
3. Plan assessment activities across all 12 PCI DSS domains.
4. Define evidence requests and responsibility handoffs.
5. Demonstrate hypothetical findings and evidence-based remediation closure.

## Explore the deliverables

| Deliverable | What it demonstrates |
|---|---|
| [Payment architecture](01-architecture/payment-flow.md) | Hosted payment redirect, card-data flow, trust boundaries |
| [Scope assessment](02-scope/scope-assessment.md) | Preliminary inventory and scoping decisions |
| [Control assessment plan](03-control-assessment/control-plan.md) | Twelve-domain review framework; no tests performed |
| [Audit evidence register](04-evidence/evidence-register.md) | Evidence requests, owners, and status |
| [Hypothetical remediation tracker](05-remediation/hypothetical-findings.md) | Sample risks and proposed corrective action |
| [Executive case study report](06-final-report/executive-report.md) | Findings boundaries, limitations, and next steps |
| [Reviewer playbook](07-tools/assessment-guide.md) | How an actual authorized assessment would proceed |
| [Detailed portfolio index](README_PORTFOLIO.md) | Project navigation and disclaimers |

Additional PDF and Excel deliverables may be found among repository files.

## What is completed vs. not completed

**Completed:** Documentation, preliminary scope model, example diagram, twelve-domain assessment plan, evidence request templates, hypothetical remediation examples, and executive narrative.

**Not performed:** Real system testing, stakeholder interviews, card-data discovery, ASV scans, PCI DSS control validation, third-party assurance verification, segmentation testing, and independent remediation retests.

**Status:** Documentation demonstration ready for review; compliance status **undetermined**.

## Website
[Visit Jamal Davison's living résumé](https://jamal-davison-live-resume.lovable.app/)

## References
- [PCI Security Standards Council document library](https://www.pcisecuritystandards.org/document_library/)
- [PCI SSC FAQ: Merchant website scope and SAQ A](https://www.pcisecuritystandards.org/faqs/is-a-merchant-website-still-in-scope-for-pci-dss-if-it-meets-all-the-criteria-for-saq-a/)

All characters, systems, findings, and business details in this case study are fictional. No sensitive cardholder data or confidential employer information is included.
