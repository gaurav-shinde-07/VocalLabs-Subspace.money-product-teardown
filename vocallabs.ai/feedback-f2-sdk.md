# F2 - VocalFlow SDK Has 0 Stars and Zero Developer Onboarding Path

**Pillar:** Features / Services
**Priority:** P0 - Ship within 2 weeks

---

## (a) Observed

VocalLabs maintains 4 public GitHub repositories under
github.com/Vocallabsai:

| Repo | Language | Stars | Forks | Last Updated |
|------|----------|-------|-------|--------------|
| vocalflow | Swift | 1 | 13 | May 21, 2026 |
| vocal-sdk | TypeScript | 0 | 0 | May 5, 2026 |
| n8n-nodes-vocallabs | TypeScript | 0 | 0 | Apr 15, 2026 |
| chrome-extension-for-tab-recording | JavaScript | 0 | 0 | Aug 2025 |

The vocal-sdk repository — the primary integration surface for any
developer wanting to build on VocalLabs — has 0 stars, 0 forks, and
0 open issues as of May 2026.

The docs site (docs.vocallabs.ai) renders a single card that says
"Updated May 27, 2026" with no API reference, no quickstart guide, and
no code examples visible to an unauthenticated visitor.

The n8n node (last updated April 2026) shows there is active
development happening — but it is completely unannounced and
undiscoverable by the developer community.

---

## (b) Problem

Developer adoption is VocalLabs' most defensible distribution channel
against US-funded competitors. Vapi's entire growth flywheel was built
on a developer-first SDK that let builders ship a working voice agent
in a weekend. Those developers then introduced Vapi into their
employers' procurement cycles — 60-70% of Vapi's early B2B pipeline
originated from developer-led internal tools.

VocalLabs is attempting to replicate this with open-source VocalFlow
(listed as a separate product on the website) but has accidentally
hidden the on-ramp.

A developer who lands on vocal-sdk finds:
- No README with a working code snippet
- No npm install badge or version indicator
- No "Hello World" voice call in under 5 lines
- No link to a sandbox where they can hear the output

They close the tab. Not because the product is bad — but because the
entry point does not exist.

This is not a minor documentation gap. It is a closed door on the
channel that compounds most efficiently for a bootstrapped company
with no paid acquisition budget.

---

## (c) Ship Instead

Execute a "Developer Day 0" sprint. The success metric is:
a developer goes from `npm install` to first live AI voice call
in under 15 minutes, with zero sales interaction.

**Week 1 - The README**

Write a vocal-sdk README that contains:
```
npm install @vocallabs/sdk
```
```typescript
import { VocalLabs } from '@vocallabs/sdk';

const client = new VocalLabs({ apiKey: 'YOUR_API_KEY' });

const call = await client.calls.create({
  toNumber: '+91XXXXXXXXXX',
  agentId: 'your-agent-id',
  language: 'hi-IN',
});

console.log('Call started:', call.id);
```
Embed a CodeSandbox or StackBlitz link so developers can run
this without even cloning the repo.

**Week 1 — Free Sandbox**

Create a developer sandbox on docs.vocallabs.ai:
- ₹500 free credits, no credit card required
- Docs fully visible without login
- Single-page quickstart that mirrors the README above

**Week 2 - Developer Content**

Publish one tutorial on dev.to and Hashnode:
"Build an AI voice agent for Swiggy merchant outreach in 20 minutes
using VocalLabs SDK"

Use a real Indian use case. English + Hinglish sample transcript.
Show actual output audio if possible.

**Week 2 - GitHub Hygiene**

Add to vocal-sdk:
- GitHub Actions CI badge (shows the repo is alive)
- npm version badge
- CONTRIBUTING.md with a clear "how to submit a PR" guide
- CHANGELOG.md with the last 3 releases

These signals are how developers evaluate whether a repo is worth
their time before reading a single line of code.

---

## Tradeoff Thinking

Free credits have a cost. Counter: set a hard cap at ₹500/user,
require phone verification (reduces abuse), and treat the cost as
CAC for the developer channel - which historically has the highest
LTV-to-CAC ratio of any B2B acquisition channel.