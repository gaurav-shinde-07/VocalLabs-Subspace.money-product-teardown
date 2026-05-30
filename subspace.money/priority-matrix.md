# Priority Matrix & Executive Summary

## Priority Matrix

| # | Feedback | Impact | Effort | Urgency | Priority |
|---|----------|--------|--------|---------|----------|
| F1 | Credential sharing broken by design | 🔴 High - churn driver + review damage | 🔴 High - escrow requires integration | 🔴 Now - reviews compounding | **P0 - Start wallet refund fix this week, escrow in Q3** |
| F2 | Homepage hero mismatch | 🔴 High - first impression kills conversion | 🟢 Low - copy + design only | 🔴 Now - every visitor sees wrong message | **P0 - This week** |
| F3 | Negotiate API invisible | 🟡 Medium - retention + referral lever | 🟢 Low - UI surfacing only | 🟡 Soon - moat is wasted | **P1 - Next sprint** |
| F4 | Admin accountability gap | 🔴 High - viral trust damage | 🟡 Medium - dispute flow + rating logic | 🔴 Now - bad reviews compound daily | **P0 - Dispute flow in 2 weeks** |
| F5 | ONDC + local marketplace moat | 🔴 Very High - only uncopyable moat | 🔴 High - ONDC cert + portal | 🟡 Soon - Fleek closing gap | **P1 - Start WhatsApp MVP now, ONDC in Q3** |

---

## Sequencing Logic

**F2 ships this week (2 days)**
It is a pure copy and design change. The homepage hero
rewrite requires zero engineering. Removing the auto-triggered
location modal requires 1 hour of frontend work. The impact
on new user conversion is immediate and measurable via
bounce rate and "Join a group" click-through rate.

**F4 dispute flow ships in 2 weeks**
The basic in-app dispute flow (submit issue → admin notified
→ auto-resolve in 24 hours → wallet refund) is a 2-sprint
feature. The rating separation (cooling-off period on
retaliatory ratings) is a database rule, not a product.
Start with these two - they directly stop the review damage.

**F1 wallet refund fix ships in parallel (1 week)**
Remove Aadhaar KYC requirement for disputes under ₹500.
Replace with Subspace wallet refund (instant). This is the
fastest trust-repair action available and the one most
directly cited in negative reviews.

**F3 surfaces in the next sprint (2 weeks)**
The Price Watch UI is a display feature - it reads data
that already exists (negotiated prices vs. retail prices)
and shows it to users. The onboarding screen addition is
one screen. Total effort: 3-4 days of product + design.

**F5 starts WhatsApp MVP now, ONDC in Q3**
The WhatsApp Business chatbot for local subscription
discovery is a 4-6 week project. Start it now so it
ships before Fleek does something similar. The ONDC
integration is a Q3 initiative — begin the certification
process now since it takes 6-8 weeks.

---

## Root Cause Analysis

All 5 feedbacks trace to a single underlying pattern:

**Subspace has built a genuinely differentiated product
but is communicating and protecting it like an MVP.**

The differentiation is real:
- ₹36.5 Cr ARR bootstrapped is extraordinary
- Negotiate API is genuinely hard to replicate
- Local subscription marketplace is a unique positioning
- Network effects from group sharing are defensible

None of this is apparent from the first 10 seconds of
using the website or app. And the trust infrastructure
protecting the core sharing behaviour is thin enough
that a few bad admin actors are generating reviews that
undo all the positive word-of-mouth the product earns.

The fixes are not about building new features.
They are about protecting and surfacing what already exists.

---

## Coverage Across All 5 Pillars

| Assignment Pillar | Feedback Covered |
|-------------------|-----------------|
| GTM & ICPs | F2 - Homepage hero mismatch + ICP conversion fix |
| Competitor Analysis | Full matrix + SWOT (01-competitive-analysis.md) |
| Features / Services | F3 - Negotiate API invisible, F4 — Admin accountability |
| UX | F1 — Credential sharing broken by design |
| Potential Collaborations | F5 - ONDC + WhatsApp Business integration |

All 5 pillars covered. No pillar has more than 2 feedbacks.
Each feedback follows the Observed → Problem → Ship Instead
structure from the assignment brief.