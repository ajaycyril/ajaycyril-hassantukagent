# What Would an AI Agent Actually Do During a Fire Alarm?

*Building a browser-based safety command centre around evidence, orchestration and human control*

A detector goes off in a villa.

Today, that usually starts a familiar chain: an event lands in a monitoring system, someone checks it, someone calls, and someone decides whether to escalate.

I wanted to see what a different experience could look like. Not a prettier alert dashboard, but a system that actually follows an incident from detection to decision.

That became **Hassantuk Command**, an interactive prototype I built to explore agentic AI for connected homes, buildings and security.

![Hassantuk Command villa scenario](https://digdeeptech.com/wp-content/uploads/2026/11/hassantuk-villas.jpg)

*The villas view in the prototype. Event data, operational actions and response activity are simulated.*

## The interesting part isn't the alarm

It's everything that should happen next.

The agent should look at the type of detector, the recent sensor history, any previous false alarms and what else is happening in the building. It should ask whether multiple signals corroborate a fire. It should contact a resident where appropriate, request more evidence, and decide which tools can help confirm the situation.

Only then should it recommend escalation.

That's the gap I wanted to make visible. A safety agent isn't just an LLM attached to a chatbot. It is an orchestration layer connecting models, evidence, tools, operating policies and people.

## Three connected worlds

I built the experience around three scenarios, because the same agent architecture should support different safety workflows without pretending they are identical.

**Villas:** a detector event becomes a risk assessment, a simulated resident interaction, drone/video verification, routing and an emergency-response handoff.

**Buildings:** floor-level context, correlated alarms and verification come before a response decision.

**Smart-home security:** suspicious activity combines with property history, visual evidence and resident confirmation before choosing a response path.

![Building incident experience](https://digdeeptech.com/wp-content/uploads/2026/11/hassantuk-buildings.jpg)

*Buildings introduce floor context, verification stages and coordination challenges.*

![Smart-home security experience](https://digdeeptech.com/wp-content/uploads/2026/11/hassantuk-security.jpg)

*Security has a different decision path, even when it shares the same orchestration backbone.*

## How I structured the agent

I found it useful to think about the platform in five parts.

**1. An evidence layer.** Sensor events alone aren't enough. The agent needs incident history, property context, confidence signals, visual evidence and location.

**2. Assessment and planning.** The orchestration layer evaluates the evidence, updates a risk assessment and selects the next bounded action. It needs explicit reasons, not just a confidence score.

**3. Tool execution.** Calling a resident, requesting camera evidence, plotting a route, running an inspection or notifying a responder are different tools with different permissions. The prototype simulates their real-world effects.

**4. Guardrails and approval.** A false alarm should stop escalation. A model failure should be visible. Any actual high-stakes external action would need policies and appropriate human oversight.

**5. A human-readable operating experience.** The operator should see what the system knows, why it acted, what it is doing now and what remains unresolved.

This is where I think the biggest design challenge lies. It's not enough for agents to be capable; they must be **legible**.

## Why I kept a deterministic engine

There's a temptation to make every demo step a live LLM call. I didn't want that.

A good exhibition demo needs reproducibility. You should be able to pause an incident, inspect a decision and replay a specific edge case without a model changing the scene unexpectedly.

So the experience separates a deterministic story engine from optional model-backed agent decisions and explanations. When live AI isn't available, the UI should not misrepresent scripted events as live reasoning.

![Incident handover and response](https://digdeeptech.com/wp-content/uploads/2026/11/hassantuk-response.jpg)

*The response timeline brings evidence, decisions and simulated handovers into one place.*

## The next technical frontier

The compelling step isn't adding another large model. It's bringing edge intelligence, network visibility and orchestration into the same operating plane.

Imagine on-device audio and computer vision identifying early warning patterns, a shared evidence model correlating them, an agent reasoning over current policy and a secure network-to-edge layer executing only authorised actions.

That means real work on model evaluation, event schemas, observability, policy enforcement, device lifecycle management, reliability and human intervention. And in safety-critical settings, none of it replaces engineering validation or regulatory approvals.

## What this project does, and doesn't, prove

Hassantuk Command is a **browser-based concept demonstration**, not a live integrated emergency system. The locations, device readings, calls, drones, dispatches and response outcomes are illustrative or simulated. Optional LLM interaction is not the same thing as real emergency autonomy, and the visuals are not evidence of a field deployment.

What the project *does* help test is an operating model: can we make the handoff from detection to investigation, verification, decision and response understandable in a single interface?

That is the interesting question for agentic AI in the physical world.

**[Try the live interactive demo](https://hassantuk-command.vercel.app/) · [Explore the GitHub showcase](https://github.com/ajaycyril/ajaycyril-hassantukagent)**

*Built as a personal technical exploration of agentic safety systems and connected environments. Not an official Hassantuk or authority deployment.*
