# FuturePays — Preliminary PCI DSS v4.0.1 Scope Assessment

**Status:** Draft, not validated  
**Prepared by:** Jamal Davison  
**Version:** 1.0 | **Date:** 2026-10-29

> Fictional educational portfolio project. No assessment findings, compliance validation, or certification is claimed.

## Business and payment flow

FuturePays is a fictional online retailer using a redirect to a third-party hosted payment page. Customer card data is assumed to be provided directly to the PSP. FuturePays is assumed to store order metadata and payment status, not full card numbers. These assumptions must be verified.

Customer browser → FuturePays storefront → PSP hosted page → payment processor → transaction status returned to FuturePays.

## Scoping principles

- The payment redirect mechanism and merchant website can impact payment data security and should be evaluated.
- Connected-to and security-impacting systems require investigation, even if they do not store PAN.
- Outsourced payment processing does not eliminate all merchant responsibilities.
- No final SAQ type or scope exclusion is asserted.

## Preliminary inventory

| System | Function | Classification | Verification required |
|---|---|---|---|
| Customer browser | External customer device | External / untrusted | Verify direct flow to PSP; no merchant-controlled capture |
| FuturePays web store | Merchant storefront and redirect | Security-impacting / in scope | Validate redirection, scripts, hosting, and administrator access |
| Hosted payment page | Third-party card collection | TPSP payment environment | Obtain TPSP AOC and payment solution architecture |
| Payment gateway / processor | Authorization processing | TPSP payment environment | Responsibility matrix and AOC |
| FuturePays app server | Checkout and order logic | Investigate / potentially security-impacting | Verify redirect creation, connectivity, and logs |
| Order database | Order reference and status | Investigate / potentially out of scope | Validate fields, logs, backups, and access paths |
| Admin workstations | Manage storefront | Investigate / potentially security-impacting | Identify privileged access and management paths |
| Identity provider | Admin authentication | Investigate / potentially security-impacting | Confirm whether it controls in-scope systems |
| Logging and monitoring | Security events | Investigate / security-impacting | Inspect logs for PAN; assess security service dependencies |
| Corporate network | General business operations | Potentially out of scope - unverified | Validate segmentation, routes and shared services |

## Evidence requests

- [ ] E-01: Current network / data-flow diagram
- [ ] E-02: Asset inventory, environment ownership, hosting details
- [ ] E-03: Redirect implementation and deployment configuration
- [ ] E-04: Log / database data-discovery results
- [ ] E-05: Admin access paths and identity configuration
- [ ] E-06: Third-party AOC and responsibility matrix
- [ ] E-07: Segmentation rules and validation results
- [ ] E-08: Applicable PCI DSS / SAQ eligibility determination
- [ ] E-09: ASV scanning applicability and evidence review

## Decisions still open

- Validate actual redirect and all connected systems.
- Verify absence of card data in merchant databases, application logs, and backups.
- Obtain PSP AOC and responsibilities matrix.
- Verify segmentation and administrative access.
- Confirm applicable PCI DSS requirements and SAQ eligibility.

## References

- [PCI SSC - Scoping and Segmentation Guidance](https://www.pcisecuritystandards.org/documents/Guidance-PCI-DSS-Scoping-and-Segmentation_v1_1.pdf)
- [PCI SSC FAQ - Merchant redirect website remains in scope](https://www.pcisecuritystandards.org/faqs/is-a-merchant-website-still-in-scope-for-pci-dss-if-it-meets-all-the-criteria-for-saq-a/)
- [PCI SSC FAQ 1588 - SAQ A e-commerce script criterion](https://www.pcisecuritystandards.org/faqs/1588/)
- [PCI SSC FAQ 1604 - ASV scanning for outsourced e-commerce](https://www.pcisecuritystandards.org/faqs/1604/)
