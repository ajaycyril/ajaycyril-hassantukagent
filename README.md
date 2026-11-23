# Hassantuk Command
### My interactive vision for the UAE's next-generation, nationwide agentic safety network

**[Explore the live interactive prototype](https://hassantuk-command.vercel.app/)** · **[Read the engineering story on DigDeepTech](https://digdeeptech.com/hassantuk-agentic-safety-command-centre/)**

## What is Hassantuk?

**[Hassantuk](https://building.moi.gov.ae/en-US/Hassantuk%20Overview/)** is a UAE Ministry of Interior and Civil Defence connected fire and life-safety initiative. **[Hassantuk for Homes](https://home.moi.gov.ae/en/index.html)** protects residential villas; the buildings programme connects fire and safety systems in commercial and residential properties to alarm receiving and verification centres. Confirmed emergency events are relayed to Civil Defence. This is existing national-scale safety infrastructure, not an invented prototype.

## My vision: from national alarm network to national Safety AI

I'm **Ajay Cyril**. Drawing on years leading connected-safety products and the Hassantuk for Homes roadmap, **I built this interactive demo** to make a possible next chapter tangible: a nationwide, agentic safety and security platform that doesn't just receive alarms, but understands events, gathers evidence, coordinates bounded actions and helps people respond.

The vision brings together **edge intelligence, secure network-to-edge management, an evidence layer, multimodal models, multi-agent orchestration, digital twins and human-authorised response**. It is a personal technical/product thesis, **not an official Hassantuk roadmap or deployed authority capability**.

> **Concept demonstration only.** All physical actions, telemetry, residents, emergency response, drone flights and visual evidence are simulated or illustrative. There is no live operational connection to authorities. Optional model calls are distinguished from deterministic scripted workflows. Do not use this prototype for actual safety decisions.

**[Read my full roadmap and engineering story on DigDeepTech](https://digdeeptech.com/hassantuk-agentic-safety-command-centre/)** · **[Read the same article here on GitHub](ARTICLE.md)**

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


## Public sources and attribution

The official [Hassantuk for Homes](https://home.moi.gov.ae/en/index.html), [Hassantuk for Buildings](https://building.moi.gov.ae/en-US/Hassantuk%20Overview/) and [UAE Government fire-safety overview](https://u.ae/en/information-and-services/justice-safety-and-the-law/fire-safety) describe the existing programmes. The future architecture and roadmap in this repository are Ajay Cyril's independent proposal, not an authority announcement. [DigDeepTech](https://digdeeptech.com/hassantuk-agentic-safety-command-centre/) is the canonical editorial version of the article.
