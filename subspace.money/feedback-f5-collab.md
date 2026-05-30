# F5 - ONDC Integration Unlocks the Local Subscription Marketplace Moat

**Pillar:** Potential Collaborations
**Priority:** P1 - Biggest long-term differentiation available

---

## (a) Observed

Subspace claims "India's first subscription marketplace for local
providers" as a key moat in the assignment brief.

After walking through the app and website, the local subscription
marketplace is:
- Not discoverable from the homepage (hero is delivery-focused)
- Not mentioned by name anywhere visible in the nav or hero
- The "Explore" tab shows primarily OTT brands (Netflix, Prime,
  Hotstar, Spotify) - the same brands every competitor also lists
- Local/hyperlocal providers (gym memberships, tiffin services,
  local newspapers, coaching classes) are present but buried
  with no dedicated section or onboarding path for new providers
- The blogs.subspace.money site has one blog post from 2023 about
  the sharing feature - no content about how local providers
  can list on the platform or what the marketplace model offers

The Subspace API (superflow.run) exists but is presented as
a developer tool - not as a marketplace onboarding portal
for a dhaba that wants to sell monthly tiffin subscriptions.

---

## (b) Problem

The local subscription marketplace is Subspace's only truly
uncopied feature. Fleek doesn't have it. GoSplit doesn't have
it. No OTT platform has it. It is the moat that can compound
into something no VC-funded competitor can quickly replicate
because it requires ground-level city-by-city onboarding
of hundreds of small providers.

But the moat is empty right now because:
1. Local providers don't know they can list on Subspace
2. There is no self-serve onboarding flow for a local business
   — they would need to contact Subspace directly
3. Users don't know to look for local subscriptions on Subspace
   because the homepage promotes OTT brands, not local ones
4. Without critical mass of local providers in each city,
   the "hyperlocal" positioning is a claim without substance

The cost of not building this: every month Subspace stays
as "yet another OTT discount app", Fleek closes the gap on
the exact features Subspace actually does well.

---

## (c) Ship Instead

Pursue a two-sided strategy: ONDC on the supply side,
WhatsApp Business on the demand side.

**Supply Side: ONDC Integration**

ONDC (Open Network for Digital Commerce) is India's government-
backed open commerce protocol, already used by 7.5 lakh+ sellers.
Subspace should integrate as an ONDC buyer-side application
that surfaces subscription-type products from ONDC sellers.

This immediately onboards thousands of local subscription
providers - gym chains, cloud kitchens, coaching institutes,
local news publishers - who are already on ONDC without
Subspace needing to sign each one individually.

The integration also gives Subspace a government-endorsed
legitimacy signal that resonates particularly well with
Tier-2 and Tier-3 city users and local business owners.

**Supply Side: Local Provider Self-Serve Portal**

Build a simple "List your subscription on Subspace" landing
page targeting local businesses:
- Business name, city, subscription type, price, slots
- Bank account for payouts
- Goes live in 24 hours after verification
- Subspace takes 8-12% commission per transaction

Promote this in WhatsApp Business groups for local business
owners in 5 target cities: Bengaluru, Hyderabad, Pune,
Chennai, Ahmedabad.

**Demand Side: WhatsApp Business Integration**

The user's discovery of local subscriptions should happen
where they already spend time — WhatsApp.

Partner with WhatsApp Business API to enable:
- "Find subscriptions near me" via Subspace WhatsApp bot
- Monthly subscription renewal reminders sent on WhatsApp
- Group payment collection for shared subscriptions via
  WhatsApp payment links
- New local provider alerts: "A new tiffin subscription
  launched near you in Koramangala — ₹1,800/month"

This creates a discovery and retention loop that lives
inside India's most-used app, reducing dependence on
users remembering to open Subspace independently.

**Flagship Metric:**
Track: number of local (non-OTT) subscription providers
listed per city vs. OTT providers.
Goal: local providers = 30% of marketplace listings within
12 months of ONDC integration.
This metric is what makes Subspace's "India's first local
subscription marketplace" claim actually true and defensible.

---

## Tradeoff Thinking

ONDC integration has technical complexity and requires
compliance with ONDC's buyer-app certification process.
Counter: ONDC buyer-app certification is a one-time effort
that permanently unlocks lakhs of sellers. The alternative
 manual provider onboarding one by one - does not scale.
The WhatsApp Business integration is simpler and can ship
first as an MVP chatbot in 4-6 weeks.