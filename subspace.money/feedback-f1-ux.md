# F1 - Credential Sharing Is Broken by Design, Not Just in Execution

**Pillar:** UX
**Priority:** P0 - Active churn driver today

---

## (a) Observed

On the /public-groups page, the "How Group Sharing Works" section
explains the model in 3 steps:

Step 1: Join a Group - pay your share
Step 2: Share Credentials - the group owner shares login details
Step 3: Enjoy Together - access premium features

Step 2 is the entire product risk condensed into one line:
"The group owner typically shares the subscription credentials
securely with all members."

The word "typically" is doing enormous work here. There is no
platform mechanism that enforces credential delivery, verifies
that shared credentials work, or protects the subscriber if
the admin changes the password or removes them after payment.

Play Store reviews confirm this plays out badly in practice:
- "subscriber doesn't allow you to login I am taking a subscription
  to Amazon prime now he logged out of me from the id"
- "An admin removed me from a group because I requested an OTP
  twice after Amazon logged me out automatically"
- "admin never replied... would advise against shared subscription
  as you're dependent on admins"
- "getting a refund is a hassle.. KYC, Aadhaar etc.. no direct
  UPI refund"

The refund flow requires Aadhaar-level KYC for what is typically
a ₹100–300 dispute. No competitor requires this level of friction
for a refund.

---

## (b) Problem

The shared subscription model's entire value proposition is
saving money through trust. But Subspace has built the financial
transaction layer (payment is instant and irrevocable) without
building the trust enforcement layer (what happens when the
admin fails the subscriber after payment).

This is a structural design flaw, not an edge case. Every new
user who joins a shared subscription group is exposed to
admin risk with no in-app safety net.

The consequences are compounding:
1. Users who get burned write 1-star reviews - the Play Store
   page has multiple visible ones
2. Users who see those reviews never join shared groups -
   reducing the network effect that is Subspace's primary moat
3. Users who fear admin abuse stay on the cheaper individual
   subscription option - cannibalising the higher-margin
   sharing business

The Aadhaar KYC refund requirement makes this worse. Asking
a user to submit a national identity document to recover ₹200
is not a refund process - it is a deterrent.

---

## (c) Ship Instead

Build a "Subscriber Protection Layer" - three specific mechanisms
that enforce trust structurally rather than relying on admin goodwill.

**Mechanism 1: Credential Escrow (not manual sharing)**

Instead of the admin manually sharing a password, Subspace holds
the credential in encrypted escrow. The subscriber gets a
one-time-use session token or a Subspace-managed login button
that authenticates them to the service without ever seeing
the raw password.

This removes the admin's ability to lock out the subscriber
because the credential never leaves Subspace's control.
GoSplit uses an escrow model for this exact reason.

**Mechanism 2: Automated Access Verification**

24 hours after payment, Subspace's system pings the shared
account to verify the subscriber's profile still has access.
If access is lost, the system:
- Sends an alert to the admin to restore access within 4 hours
- Automatically initiates a partial refund if not restored
- Flags the admin's trust score

This turns the current reactive complaint model into a
proactive protection model.

**Mechanism 3: Instant Wallet Refund, No KYC**

For disputes under ₹500, offer an instant refund to Subspace
wallet balance — no Aadhaar, no KYC, no call required.
The wallet balance can be used on the next subscription.
This is the same model Zomato and Swiggy use for food
delivery complaints and it works because the platform
absorbs small dispute costs to protect retention.

Reserve the Aadhaar KYC requirement for refund requests
above ₹1,000 to a bank account.

---

## Tradeoff Thinking

Credential escrow requires technical integration with each
OTT platform's login flow - complex and some platforms may
block it. Counter: start with the top 5 platforms by GMV
(Netflix, Amazon Prime, Spotify, YouTube Premium, Hotstar).
The automated verification ping is simpler - just check if
the subscriber's profile name still appears on the account
and is achievable within 2 sprints.