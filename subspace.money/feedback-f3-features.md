# F3 - Negotiate API Is Subspace's Strongest Moat but Invisible to Users

**Pillar:** Features / Services
**Priority:** P1 - Unrealised revenue and retention lever

---

## (a) Observed

The assignment brief lists "Negotiate API: automated price
negotiation = hard to replicate" as one of Subspace's key moats.

After a full walkthrough of subspace.money, the Play Store
listing, the blogs, and the About Us page - the Negotiate API
is mentioned exactly zero times to users anywhere in the app
or website.

The About Us page describes the business model as:
"Subspace is a platform that allows users to make group purchases
of gift cards, which helps them save money. Our revenue model is
based on taking a small percentage of the total transaction value
as a commission fee."

There is no mention of automated negotiation with brands.
The Play Store description mentions discounts (up to 80% off)
but attributes these to "Guaranteed discounts" with no
explanation of how Subspace secures them.

The SuperFlow / Subspace API documentation (superflow.run/docs)
is a separate product site - completely disconnected from the
user-facing app experience.

---

## (b) Problem

The Negotiate API is the one feature that no competitor -
not Fleek, not GoSplit, not any manual WhatsApp group - can
replicate without significant engineering investment.

It should be Subspace's primary acquisition story:
"We automatically negotiate better prices with brands on
your behalf - every month, in the background, without you
doing anything."

Instead it is invisible. Users see discounts but attribute
them to Subspace being a bulk buyer, not to an intelligent
negotiation engine that is actively working for them.

This is a missed retention and word-of-mouth opportunity.
When users understand that Subspace is actively fighting
for cheaper prices on their behalf, it creates an emotional
connection with the product that purely transactional apps
cannot replicate.

The invisibility also has a direct financial cost: if users
don't know the Negotiate API exists, they cannot invite
friends with "you should download Subspace, it automatically
negotiates your subscription prices down" - which is the
most compelling referral hook the product has.

---

## (c) Ship Instead

Make the Negotiate API visible as a user-facing feature called
"Price Watch" - reframe the background engine as an active
assistant the user can see working.

**In-app: Price Watch tab**

Add a "Price Watch" section in the app showing:
- Current prices Subspace has negotiated for subscriptions
  you own vs. the standard retail price
- "You saved ₹X this month via Price Watch"
- Upcoming negotiations: "Your Spotify plan renews in 14 days.
  We're negotiating the best rate for you."
- A simple toggle: "Auto-negotiate my renewals: ON/OFF"

**Onboarding moment**

During the 3-step onboarding flow, add one screen:
"Subspace automatically negotiates better prices with brands
every month. You never pay full price again."
Show a before/after price comparison: ₹199/month → ₹89/month.
This single screen will increase day-1 retention because
it gives users a reason to stay beyond the first transaction.

**Homepage hero (link to F2 fix)**

Include "Auto-negotiated prices" as one of the three value
propositions on the redesigned homepage hero:
"Split costs + auto-negotiate prices + track everything. Subspace."

**Blog / content**

Write one transparent post: "How Subspace's Negotiate API works —
and how much we've saved users in FY25."
Use aggregate, de-identified data. If the numbers are good
(they likely are at ₹36.5 Cr ARR scale), this post becomes
the most-shared piece of content Subspace has ever published.

---

## Tradeoff Thinking

Making the negotiation engine visible creates expectation
management risk - if a negotiation fails or a price goes up,
users may blame Subspace. Counter: frame the feature as
"we always try to get you the best available price" not
"prices will always go down." The transparency of trying
builds more trust than the opacity of silence, even when
outcomes are imperfect.