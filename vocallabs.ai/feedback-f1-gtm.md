# F1 - No Pricing Page = a GTM Wall for the Exact ICP You Need

**Pillar:** GTM & ICPs
**Priority:** P0 - Ship this week

---

## (a) Observed

The website's primary CTA is "GET STARTED ⚡ 2 mins" which routes to
a /contact (demo request) form. There is a /pricing-policy URL listed
in the footer, but navigating to it redirects back to the homepage —
pricing information is completely absent from the entire site.

Every direct competitor publishes pricing or at minimum a tiered plan
structure:
- Vapi: $0.05/min publicly listed + usage calculator
- Retell AI: $0.07–0.15/min with plan breakdown
- Bland AI: Starter/Build/Scale tiers published with per-minute rates
- Synthflow: Flat + usage tiers, transparent page

VocalLabs has none of the above. The only path to pricing is booking
a demo call.

---

## (b) Problem

The ICP for VocalLabs at this stage should be the mid-market B2B buyer:
a Head of CX or CTO at a D2C brand, NBFC, or hospital chain with
200–2,000 agents, a ₹5–20L/month opex problem, and the authority to
sign without a 3-month enterprise procurement cycle.

This buyer does not book demos blindly.

Gartner (2025) research shows 77% of B2B SaaS buyers complete more
than 50% of their vendor evaluation before ever speaking to sales.
Without a pricing signal, they self-disqualify VocalLabs and move to
Retell or Synthflow where they can evaluate the fit in 10 minutes on
their own.

The broken /pricing-policy redirect compounds the problem. For BFSI and
GovTech evaluators — the exact buyers VocalLabs is targeting based on
its deployment portfolio — a broken footer link signals carelessness
in a product that is supposed to handle mission-critical calls.

VocalLabs is doing outbound-only sales with no inbound assist, at a
stage where every competitor has self-serve pricing. The funnel leaks
before it even starts.

---

## (c) Ship Instead

Build a 3-tier pricing page targeting two distinct ICPs simultaneously.

**Tier 1 - Starter (self-serve)**
- ₹4/min all-in, 500-minute free trial, card-on-file signup
- No sales call required
- Targets: lean SMBs, agency developers, internal tools teams

**Tier 2 - Growth (assisted)**
- ₹2.5/min at committed 10,000 min/month
- Includes onboarding call + dedicated Slack channel
- Targets: mid-market CX teams, NBFCs, D2C brands

**Tier 3 - Enterprise**
- Custom SLA, DPDP Data Protection Addendum, dedicated support
- CTA = book demo (same as current flow)
- Targets: BFSI institutions, government departments

**Add a ROI calculator on the same page:**
Input: number of human agents →
Output: ₹X saved per month vs current cost

Use ₹18–25/min as the human agent benchmark (standard India BPO rate),
compare against ₹2.5–4/min AI rate. The math is compelling — show it.

**Fix the /pricing-policy redirect immediately.**
This is a 5-minute engineering task that is currently damaging
credibility with every enterprise visitor who clicks the footer.

---

## Tradeoff Thinking

Publishing pricing risks competitors undercutting on paper.
Counter-argument: competitors already know their own pricing; the only
people being kept in the dark are potential customers.

Value-based tier framing (₹/min all-in vs. component-based pricing
like Vapi) actually positions VocalLabs favorably — it removes the
anxiety of unexpected cost stacking that is the #1 complaint about
Vapi in developer communities.