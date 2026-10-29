# Proposed FuturePays Payment Flow

**Status: Conceptual architecture only; not deployed or validated.**

```mermaid
flowchart LR
 C[Customer browser] -->|HTTPS shopping| W[Merchant storefront]
 W -->|Hosted checkout redirect| P[PSP hosted payment page]
 C -->|PAN entered at PSP| P
 P -->|Card data| G[Processor / network]
 G -->|Authorization outcome| P
 P -->|Authenticated status callback| O[Merchant order service]
 O -->|Order ID, status, reference only assumed| D[(Order database)]
 A[Privileged administrators] --> W
 W -.->|Security events| L[Log monitor]
 subgraph Merchant[FuturePays merchant-managed]
 W
 O
 D
 A
 L
 end
 subgraph PSP[Third-party payment provider]
 P
 G
 end
```

Cardholder data is **assumed** to be submitted directly to the PSP-hosted page. FuturePays is assumed to receive reference and order status only. Verify by inspecting source code, web behavior, data stores, logs, backups and PSP contract.

**Scoping caution:** The merchant storefront and redirect logic can impact payment security even without merchant PAN storage; this is not an SAQ eligibility determination.