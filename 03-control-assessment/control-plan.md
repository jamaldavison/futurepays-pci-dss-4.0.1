# PCI DSS v4.0.1 — Control Assessment Plan

**Domain-level planning matrix, not a reproduction of PCI DSS subrequirements or a completed compliance evaluation.** Verify precise applicability and testing procedures against the official standard.

| Domain | Planned examination | Evidence requested | State |
|---|---|---|---|
| 1 Network controls | Boundary rules, connectivity, changes | Firewall rules, diagrams, approvals | Not tested |
| 2 Configuration | Hardened baselines and defaults | Baseline and configuration exports | Not tested |
| 3 Stored account data | Card-data absence and retention | Discovery, logs, backup review, TPSP AOC | Not tested |
| 4 Transmission | Encrypted processing flows | TLS and integration configuration | Not tested |
| 5 Malware protection | Endpoint and applicable server controls | Coverage, policy, detection | Not tested |
| 6 Secure software | Patching and integrity of payment redirect | Change approvals, scan results, code review | Not tested |
| 7 Access restriction | Least privilege | Roles, approvals, access reviews | Not tested |
| 8 Authentication | Admin identity and MFA | Authentication and lifecycle evidence | Not tested |
| 9 Physical access | Relevant data center or provider physical security | Physical policy and provider evidence | Not tested |
| 10 Logging | Event sources and monitoring | Logging settings and redacted samples | Not tested |
| 11 Testing | Scans, merchant website ASV applicability, test evidence | ASV and test plans | Not tested |
| 12 Governance | Policies, scope maintenance, vendor responsibilities | Policies, AOC, responsibility matrix | Not tested |

Every real control test would record requirement ID, population, sample, owner, period, observation, evidence URI, conclusion and reviewer. Never issue pass/fail based only on these planned steps.

Official: https://www.pcisecuritystandards.org/document_library/