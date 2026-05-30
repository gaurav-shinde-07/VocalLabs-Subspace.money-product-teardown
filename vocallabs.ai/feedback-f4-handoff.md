# F4 - Hybrid AI↔Human Handoff Has No Compliance or Observability Layer

**Pillar:** Features / Services
**Priority:** P0 - Currently blocking enterprise deals

---

## (a) Observed

VocalLabs lists "Hybrid model: seamless AI ↔ live agent transitions"
as a core product feature on the homepage.

However, after reviewing the website, docs site, and all public
GitHub repositories, there is no documentation covering:

- What triggers a handoff (rules-based threshold vs. AI confidence
  score vs. customer explicit request vs. script dead-end?)
- What context the live agent receives when a call is transferred
  (full transcript? last 3 turns? emotion flag? intent summary?)
- How the handoff event is logged for regulatory audit purposes
- Whether the customer hears a disclosure utterance confirming they
  are now speaking to a human agent
- Whether handoff events are exportable for DPDP / TRAI compliance

Retell AI, by comparison, publishes detailed documentation on their
call transfer logic including the exact real-time context packet
structure sent to live agents on transfer.

VocalLabs' entire handoff story exists only as a marketing bullet.

---

## (b) Problem

VocalLabs' two largest deployment categories are:
1. BFSI - banks, NBFCs, payment companies (RBI FPC compliant)
2. GovTech - 112 emergency calls, cybercrime workflows (TRAI regulated)

Both sectors require, under Indian regulatory frameworks:
- Auditable records of every AI-to-human handoff event
- Clear disclosure to customers when they are speaking with an AI
  vs. a human agent
- Consent and call recording compliance under DPDP 2023

A handoff feature without documented audit logging is not just a
product gap - it is a compliance liability in the exact sectors
where VocalLabs is trying to win its biggest contracts.

More immediately: enterprise procurement teams include legal and
compliance reviewers who will ask for handoff documentation during
the RFP stage. Without it, deals stall at legal review.

There is also a direct user experience cost. If the live agent
receives no context summary from the AI call, they ask the caller
to repeat everything from the beginning. This is the single most
cited complaint in voice AI deployment post-mortems across Retell,
Bland, and Vapi enterprise customer reviews. The customer experience
built by the AI call is immediately erased.

---

## (c) Ship Instead

Ship the "Handoff Intelligence Pack" - both as a product feature
and as a published compliance document on the website.

**Feature: Configurable Handoff Triggers**

In the Call Flow Builder, let customers configure:
- Confidence score threshold (e.g., AI confidence < 70% → escalate)
- Emotion detection flag (customer sentiment = distressed → escalate)
- Explicit customer request ("speak to a human")
- Maximum turn count reached without resolution
- Script dead-end (no matching intent for 2 consecutive turns)

**Feature: Agent Briefing Card**

On every handoff, auto-generate and deliver a 3-line briefing card
to the live agent via screen pop, WhatsApp, or CRM webhook:
Customer: [Name]
Intent: [e.g., EMI overdue — ₹3,200 — requesting extension]
Sentiment: [Frustrated — raised voice in turns 4 and 6]
Last AI response: [Offered 7-day extension, customer did not confirm]

**Feature: DPDP Audit Log**

Log every handoff event with:
- Timestamp (IST)
- Trigger reason (from the configured list above)
- Call recording segment flag
- Agent ID who received the transfer
- Customer consent status at time of transfer

Export as a CSV or integrate with existing compliance dashboards.

**Feature: Mandatory Disclosure Utterance**

Before every handoff, the AI must say:
"Please hold for a moment — I am connecting you to a team member
who will be able to assist you further."

This is legally required under Indian consumer protection norms and
is a trust-building signal for the customer.

**Documentation: Publish the VocalLabs Handoff Spec**

Write a 2-page PDF titled "VocalLabs Handoff Compliance Spec"
covering all of the above. Host it on docs.vocallabs.ai and link it:
- From the enterprise sales deck
- From the website's security/compliance section
- In response to any BFSI or GovTech RFP that asks about handoff

This document alone can unblock deals that are currently stalled
at the legal review stage.

---

## Tradeoff Thinking

Configurable triggers add complexity to the Call Flow Builder UI.
Counter: expose them as advanced settings with sensible defaults
(confidence < 65%, explicit request). Most customers will use
defaults - power users will configure. The compliance logging is
non-negotiable regardless of UI complexity.