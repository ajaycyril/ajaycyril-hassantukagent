# Live demo guide

**Visit:** https://hassantuk-command.vercel.app/

The experience demonstrates three workflows:

1. **Villa fire response.** Start the homes scenario, review sensor and incident evidence, follow the risk assessment, simulated resident contact, visual/drone verification, routing and response handover.
2. **Building fire response.** Change to the buildings scenario and examine property/floor context, response routing, verification and action history.
3. **Smart-home security.** Choose the security scenario to see intrusion signals, camera/resident verification and a simulated response path.

Observe how the agent panel explains decisions, how the scene updates alongside action receipts, and whether response outcomes match current evidence.

### Limitations
This is not a real emergency response system. Telemetry, callers, homes, responders, drones and dispatches are synthetic or illustrative; no real public-service integrations are implied. In a hosted instance, AI calls may require server-side credentials and access control. Treat any model output as a demonstration, not an authoritative safety assessment.

### Images
The README embeds genuine QA screenshots from a November 2026 test run of the interface. They may differ from later iterations of the live demo.

### Owner handover
Before repointing the production deployment:
- Audit full app source, videos, fonts, maps and third-party media licences.
- Complete secret scanning and code review; check server-side environment variable requirements.
- Run dependency installation, automated tests and production build.
- Deploy a new Vercel preview and manually test all three scenarios in desktop, mobile, English and Arabic.
- Only then update the original project's Git settings or transfer the Vercel project to a new team.
