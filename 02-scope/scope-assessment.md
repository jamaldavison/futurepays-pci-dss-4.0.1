# FuturePays PCI DSS Scope Assessment — DRAFT

**Fictional / unvalidated.** Hosted redirect model; no real environment tested.

| Component | Preliminary view | Validation needed |
|---|---|---|
| Merchant storefront and redirect | Security-impacting / merchant scope | Code, hosting, redirects, ASV applicability |
| Hosted payment page and processing | Third-party payment environment | Current TPSP AOC and responsibility matrix |
| Merchant application | Scope TBD | Connections and role in checkout |
| Order database | Scope TBD | Validate no PAN in tables, logs, backups |
| Admin workstations | Security-impacting if managing checkout | Access paths and privilege |
| Identity platform | Security-impacting if controlling merchant systems | MFA, RBAC and dependencies |
| Logging / monitoring | Scope TBD | Shared controls; PAN absence |
| Office network | Potentially excluded, not validated | Segmentation and paths |
| Customer browser | External/untrusted | Redirect authenticity |

**Open assumptions:** no merchant PAN storage; wholly TPSP-hosted card entry; PSP compliance; secure merchant redirects; unverified segmentation.

## Assessment gate
Before scope sign-off: validate inventory and data flow, inspect the redirect and dependencies, obtain TPSP assurance, check segmentation, determine applicable PCI DSS requirements and confirm reporting path with acquirer or assessor.

Reference: https://www.pcisecuritystandards.org/faqs/is-a-merchant-website-still-in-scope-for-pci-dss-if-it-meets-all-the-criteria-for-saq-a/