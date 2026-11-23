# Architecture: Hassantuk Command

Hassantuk Command is a **concept prototype**, implemented in the existing demo as a Vite/React browser interface with Vercel serverless API routes. The showcase focuses on making end-to-end safety orchestration visible and auditable.

```text
┌────────────────────────────────────────────────────────────┐
│ Connected homes / buildings / security (simulated events)  │
└─────────────────────────────┬──────────────────────────────┘
                              ▼
┌────────────────────────────────────────────────────────────┐
│ Ingestion & contextual evidence                             │
│ Detectors · history · property context · video · geography  │
└─────────────────────────────┬──────────────────────────────┘
                              ▼
┌────────────────────────────────────────────────────────────┐
│ Safety orchestration                                         │
│ Deterministic scenarios  |  optional live agent             │
│ Risk assessment · specialist tools · decisions · receipts   │
│ Policies and human review for high-stakes transitions       │
└─────────────────────────────┬──────────────────────────────┘
                              ▼
┌────────────────────────────────────────────────────────────┐
│ Interactive command centre                                   │
│ National/property views · conversation · evidence · replay  │
│ Routing · drone / responder simulation · incident summary   │
└────────────────────────────────────────────────────────────┘
```

**Design principles**

- Separate event truth and evidence from the presentation narrative.
- Require explicit operation receipts and reflect failures rather than showing success optimistically.
- Provide deterministic presentation fallback if live model or communications calls are unavailable.
- Keep sessions, keys and third-party credentials server-side.
- Explicitly label simulated interventions.
- A real deployment would additionally require integrations, security reviews, privacy safeguards, regulator approvals, service guarantees and operational validation.
