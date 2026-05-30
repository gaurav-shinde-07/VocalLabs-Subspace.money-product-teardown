# F2 - Homepage Hero Positions Subspace as a Delivery App, Not a Subscription Platform

**Pillar:** GTM & ICPs
**Priority:** P0 - First impression is wrong for every new visitor

---

## (a) Observed

The subspace.money homepage hero section (the very first thing
a new visitor sees) shows:

- A location selector modal that appears immediately on load
  asking: "Detect my location" with fields for address, floor,
  landmark — the same flow as Blinkit, Zepto, or Swiggy Instamart
- Primary headline text: "Delivery in minutes"
- A "Quick search" bar in the nav

Below this first fold, the page shows "Favourite Brands" and
"Shared Subscriptions" — the actual product.

The login/signup flow is "Continue with WhatsApp OR Phone Number."
There is no intro screen, no value proposition statement, no
explanation of what Subspace does before asking for your location
or login.

The tagline in the HTML meta description says:
"Manage subscriptions, share costs, and discover new services"
— but this text is never visible on the actual page a user lands on.

---

## (b) Problem

A first-time visitor to subspace.money in 2026 sees a location
picker and "Delivery in minutes" - and has no idea they are on
a subscription management + sharing platform.

This is a direct GTM failure because it means:
- Word-of-mouth referrals ("check out Subspace, it saves you
  money on Netflix") land on a page that looks like a grocery
  delivery app. The cognitive mismatch causes immediate bounces.
- Paid or organic search users searching "share Netflix India"
  or "subscription management app India" land on a page with
  zero visible copy that confirms they're in the right place.
- The website's most powerful conversion copy — ₹36.5 Cr ARR,
  bootstrapped profitable, India's first subscription marketplace,
  up to 80% off on OTT subscriptions — appears nowhere above
  the fold.

Subspace's actual ICP is a 20-28 year old urban Indian who is
paying for 4-6 individual OTT/digital subscriptions and has
just realised they can split them with friends to save ₹400-800/month.
Nothing on the homepage speaks to that person in the first 3 seconds.

---

## (c) Ship Instead

Redesign the homepage hero with a 3-element structure that
converts the actual ICP instead of confusing them.

**Element 1: Headline that states the value in rupees**
Current: "Delivery in minutes" (wrong product category)
Replace with: "Save ₹500/month on Netflix, Prime & Spotify.
Split subscriptions with friends on Subspace."

This is the Jobs-To-Be-Done headline. It names the specific
pain (paying full price for OTT), the specific solution
(splitting with friends), and the specific outcome (₹500 saved).

**Element 2: Social proof above the fold**
Add one line below the headline:
"₹36.5 Cr saved by Indians. Bootstrapped. Profitable."
This is a trust signal that no competitor can match and it
is currently buried nowhere on the homepage.

**Element 3: Two clear CTAs for two ICPs**
- "Join a Shared Plan" → routes to /public-groups
  (for the user who wants to save immediately)
- "List My Subscription" → routes to admin signup
  (for the user who wants to earn by sharing their extra seats)

Move the delivery/rental flow to a separate tab or secondary
navigation item — it is a real feature but it should not
be the homepage's opening statement for a subscription platform.

**Fix the location modal trigger:**
Do not open the location modal on homepage load for new visitors.
Trigger it only when a user taps "Delivery" or "Rentals" explicitly.
The current behaviour creates friction and confusion before the
user has even understood what the app does.

---

## Tradeoff Thinking

Moving delivery off the hero could reduce rental/delivery GMV
from homepage traffic. Counter: delivery and rental users are
already in the app — they navigated there intentionally.
The homepage hero should optimise for first-time conversion
of the subscription ICP, which is Subspace's highest-LTV
and most word-of-mouth-friendly user type.