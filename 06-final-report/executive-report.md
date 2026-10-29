# FuturePays — PCI DSS v4.0.1 Portfolio Case Study Report

**Educational report | Not a ROC / SAQ / AOC | Compliance outcome undetermined**

## Executive summary
FuturePays is a fictional retailer using a hosted PSP redirect. This architecture may avoid merchant-side card-number collection but does not automatically exclude the merchant website or security-impacting supporting services from PCI DSS scope.

## Portfolio deliverables prepared
- Proposed payment architecture and trust-boundary diagram.
- Preliminary inventory and scope assumptions.
- Assessment plan across 12 major PCI DSS domains.
- Ten-item audit evidence request register.
- Four clearly hypothetical remediation scenarios.
- Documented follow-up and assurance strategy.

## No fieldwork performed
There were no interviews, penetration tests, ASV scans, merchant data-discovery tests, privileged access reviews, PSP AOC checks, segmentation validations, control observations or remediation retests.

## Priority roadmap
1. Verify actual integration and inventory.
2. Validate merchant PAN absence in database, logs, backups and web layer.
3. Obtain PSP AOC and responsibility allocation.
4. Verify redirect protection, hosting, admin security and connectivity.
5. Determine SAQ and exact requirements with acquirer / assessor.
6. Execute authorized fieldwork and record actual evidence-backed findings.

**Conclusion:** A demonstration of audit-readiness planning, **not** proof of implementation or compliance.