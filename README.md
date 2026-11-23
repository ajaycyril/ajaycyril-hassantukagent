# Hassantuk Command
### A browser-based agentic safety command centre for connected homes, buildings and smart-home security

**[Explore the live interactive prototype](https://hassantuk-command.vercel.app/)** · **[Read the engineering story on DigDeepTech](https://digdeeptech.com/hassantuk-agentic-safety-command-centre/)**

Hassantuk Command explores a simple question: **what if a safety alarm started an intelligent, evidence-led response instead of just another notification?**

The demonstrator brings together simulated connected-device events, risk assessment, resident contact, contextual history, camera/thermal evidence, drone verification, routing, responder handoff and an AI agent interface in a single command-centre experience.

> **Prototype / demonstration only.** This is an independent technical showcase of a *proposed* agentic safety orchestration experience, not an official operational Hassantuk system or announcement. Sensor readings, sites, phone calls, notifications, drones, emergency dispatch, response times and visual media are illustrative or simulated. There is no live connection to emergency authorities. Nothing here should be used to make real-life safety decisions.

## Demo gallery

| Connected villas | Connected buildings |
| --- | --- |
| ![Hassantuk Command villas scenario](https://digdeeptech.com/wp-content/uploads/2026/11/hassantuk-villas.jpg) | ![Hassantuk Command buildings scenario](https://digdeeptech.com/wp-content/uploads/2026/11/hassantuk-buildings.jpg) |
| Fire event detection, risk assessment and agent workflow | Multi-floor incident context, verification and response planning |

| Smart-home security | Incident response |
| --- | --- |
| ![Smart-home security scenario](https://digdeeptech.com/wp-content/uploads/2026/11/hassantuk-security.jpg) | ![Incident completion screen](https://digdeeptech.com/wp-content/uploads/2026/11/hassantuk-response.jpg) |
| Intrusion scenario and evidence-driven decisions | Simulated handover, action history and completion |

## Three scenarios
**Homes / Villas:** detector signals and home context → dynamic risk assessment → resident communication and evidence request → optional visual/drone verification → simulated civil-defence dispatch and incident closure.

**Buildings:** building-level alarm and floor context → correlated signals and prior history → scene verification → human-reviewed response plan → simulated responder coordination.

**Smart-home security:** event correlation → property history → video or resident verification → confidence-aware, human-in-the-loop response decisions.

## What the architecture demonstrates
```text
Connected properties and safety devices (simulated telemetry)
        ↓
Evidence and context layer
 • event history • sensor signals • visual evidence • geographic context
        ↓
Agent orchestration
 • investigation • risk scoring • tool selection • bounded actions
 • policy checks • confidence, receipts and human approval
        ↓
Experience and response layer
 • live command centre • resident interactions • maps and route plans
 • simulated drone / responder coordination • incident audit trail
```

The design separates a **deterministic demo scenario engine**, which keeps exhibition runs reproducible, from **optional LLM-powered agent decisions and explanations**, which require separate runtime configuration. The visible user journey does not prove that a live model made every decision.

## Key engineering ideas
- Evidence-grounded risk scores and decision receipts instead of opaque "AI says so" automation.
- Coordinated workflows across sensors, video, routing, communications and response units.
- A clear human-in-the-loop boundary around high-stakes actions.
- Repeatable, visually comprehensible demonstrations of both escalation and false-alarm closure.
- English/Arabic command-centre experience and interactive national/property views.
- Runtime keys and access configuration must stay server-side; public source must never contain credentials.

## Explore
- **Live prototype:** https://hassantuk-command.vercel.app/
- **Detailed portfolio story:** https://digdeeptech.com/hassantuk-agentic-safety-command-centre/
- **Technical walkthrough:** [ARCHITECTURE.md](ARCHITECTURE.md)
- **Demo scenarios and limitations:** [DEMO_GUIDE.md](DEMO_GUIDE.md)

## Source and deployment
This repository currently holds the **public showcase and handover documentation**. The original Vite/React application remains deployed separately through Vercel CLI. The production source, dependencies and media bundle must be reviewed and migrated to a versioned branch before switching the running app's Git source. **Do not treat this showcase repository as a complete production application.** Never commit passwords, live API tokens, simulated residents' private data, or internal response configuration.

## Attribution and use
Portfolio prototype presented by Ajay Cyril on [DigDeepTech](https://digdeeptech.com). Hassantuk, Etisalat and authority names and marks belong to their respective owners. This showcase does not imply their endorsement. Third-party visual media may carry separate rights; do not redistribute media without checking its provenance and licence.
