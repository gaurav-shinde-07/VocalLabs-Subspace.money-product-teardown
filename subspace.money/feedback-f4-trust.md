# F4 - Admin Power Without Accountability Is Destroying Network Effects

**Pillar:** Features / Services + UX
**Priority:** P0 - Viral negative reviews are compounding

---

## (a) Observed

Multiple Play Store reviews (verified, recent) describe the
same pattern:

Review 1:
"An admin removed me from a group because I requested an OTP
twice after Amazon logged me out automatically. After I rated
that experience 1 star, I unexpectedly received several 1-star
ratings and started getting removed from other newly joined
groups as well."

Review 2:
"Even though the amount was refunded to my wallet, the situation
felt unfair and biased. It seems that some admins prioritize
protecting their RATING rather than handling issues in a fair
and transparent way."

Review 3:
"subspace make very bad rule for the user once if you pay then
you lose your money.. if the subscriber doesn't allow you to
login I am taking a subscription to Amazon prime now he logged
me out from the id and subscription doesn't refund the amount."

The pattern is: admin has unilateral power to remove subscribers,
subscribers have no appeal mechanism inside the app, and the
only recourse is writing a negative Play Store review and hoping
Subspace responds.

Subspace's own response to these reviews is a customer support
phone number - which one reviewer noted was the wrong number.

---

## (b) Problem

Subspace's primary growth engine is network effects: the more
people join groups, the more people invite friends, the more
valuable the platform becomes.

Admin abuse is a direct attack on this growth engine because:
1. A user who gets removed unfairly does not just churn -
   they actively warn their network. In India, where
   financial trust is highly word-of-mouth-driven, one bad
   experience shared in a WhatsApp group of 50 people can
   prevent 10-15 potential new users from downloading the app.
2. The review-retaliation pattern (admin gives bad reviews
   to users who complain) means the rating system - which
   is supposed to create accountability - has been captured
   by admins who have more to lose from bad ratings than
   subscribers do.
3. Every subscriber who gets burned becomes a permanent
   non-user of the shared subscription feature - they may
   continue buying individual subscriptions but the
   higher-margin, higher-LTV sharing behaviour is gone.

At ₹36.5 Cr ARR, Subspace's growth ceiling is the trust ceiling.
This is the trust ceiling.

---

## (c) Ship Instead

Build an "Admin Accountability System" - three mechanisms
that rebalance power between admins and subscribers.

**Mechanism 1: Dispute Resolution Flow (in-app)**

Replace the current "call this number" support path with a
structured in-app dispute flow:

1. Subscriber taps "I have a problem with this group"
2. Describes issue from a menu: "Lost access", "Admin removed
   me unfairly", "Credentials stopped working", "No response"
3. Subspace sends admin a 24-hour resolution notice
4. If unresolved in 24 hours: automatic partial refund to
   wallet + admin trust score decremented
5. If resolved: dispute closes, no penalty

This removes human support from small disputes entirely and
creates an automated enforcement loop.

**Mechanism 2: Separation of Rating Systems**

Currently, admin ratings and subscriber ratings appear to
influence each other based on reviews. Create two separate,
non-retaliatory rating dimensions:
- "Credential reliability" - did the admin deliver working
  access on time? (rated by subscribers only)
- "Subscriber behaviour" - did the subscriber follow group
  rules? (rated by admins only)

Make it technically impossible for an admin to rate a subscriber
immediately after the subscriber files a complaint - 72-hour
cooling-off period on admin-initiated ratings.

**Mechanism 3: Admin Trust Badge with Public Criteria**

Display a visible trust badge on every public group listing:
- "Verified Admin" (phone + email verified)
- "Reliable" (0 disputes in last 90 days)
- "Top Admin" (10+ successful subscriptions, 4.5+ rating)

New subscribers should be able to filter public groups by
trust tier. This creates a positive incentive for admins
to maintain clean records rather than purely protecting
their star rating.

---

## Tradeoff Thinking

Automated refunds for unresolved disputes will cost money
in the short term. Counter: calculate the LTV of a retained
subscriber vs. the average dispute amount. If the average
dispute is ₹200 and a retained subscriber generates ₹800/year,
absorbing the dispute cost has a 4x positive ROI.
The dispute cost is also recoverable from admin penalties
(reduce admin payout on disputed transactions).