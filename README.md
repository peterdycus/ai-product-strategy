# Enterprise.com vehicle rental site

> Some customers will prefer to use an AI agent to find and book the right rental vechicle for their needs.

---

## Strategy at a Glance

| Component | Module | Status | Key Artifact |
|-----------|--------|--------|-------------|
| **The Bet** | M1 | [x] | `01-the-bet/` |
| **The Moat** | M2 | [x] | `02-the-moat/` |
| **The Margin** | M3 | [x] | `03-the-margin/` |
| **The Contract** | M4 | [x] | `04-the-contract/` |
| **The Guardrails** | M5 | [x] | `05-the-guardrails/` |
| **The Pitch** | M6 | [x] | `06-the-pitch/` |

---

## The Bet (M1)

**What we're building, for whom, why now.**

- **Product:** Enterprise.com vehicle rental site
- **AI Value Archetype:** Copilot
- **Vulnerability Scores:** _(add: Moat _/5 · Data _/5 · Platform _/5)_
- **Top Risk:**
- **Confidence:** _(add: H / M / L)_
- **Prototype:** (https://roam-and-reserve-ai.lovable.app)
- **Kill Criteria:** If adoption is below 20% in first four months, kill or pivot.

→ Details: [`01-the-bet/`](01-the-bet/)

---

## The Moat (M2)

**Why this won't get copied in 6 months.**

- **Data Flywheel Score:**
- **Weakest Loop:** Correction Lop
- **Top Encroachment Threat:** Muse
- **Encroachment Defense:** ---
- **Vendor Portability:** _(add: Ready / Partial / Locked)_

→ Details: [`02-the-moat/`](02-the-moat/)

---

## The Margin (M3)

**Will this make money or bleed it?**

- **Gross Margin (current):**
- **Gross Margin (AI-adjusted):**
- **Pricing Model:** hybrid
- **Pricing Today → Tomorrow:** $0 → $0
- **Total AI COGS / unit:**
- **Cascading Strategy:** Triage: **Frontier model:**; frontier: **Routing rule:** 80% / 20%; ratio 80 %
- **Net Margin Shift:** # Margin Calculator, Module 3
- **Break-even at:**

→ Details: [`03-the-margin/`](03-the-margin/)

---

## The Contract (M4)

**Why users will trust a probabilistic system.**

- **Reliability Target:**
- **Golden Dataset:**
- **Confidence UX:**
- **HITL Architecture:** **Trigger:** Confidence is less than 50%
- **Failure Mode Coverage:** *What failure mode did your partner find that you missed?*

→ Details: [`04-the-contract/`](04-the-contract/)

---

## The Guardrails (M5)

**What breaks when this scales, and what compounds.**

- **Compounding System:** | Loop | Input | Output | Compounds? | Status | |------|-------|--------|-----------|--------| | Recursive Learning | user corrects a location | learns and modifies the location | Y | broken | | Cross-Domain Transfer | u…
- **Governance Posture:** booking of rental vechicle Excludes: customer service requests
- **Autonomy Boundaries:** customer service request are sent to customer service, auto. user can't find their rental, human approval required. rentals not available in their location, human approval required.
- **Escalation Triggers:** 1. confidence is <70% on finding a rental at the location 2. confidence is <70% on finding a location 3. customer message is asking for help with a technical issue or loyalty question it gets flagged and sent to customer…
- **Audit Cadence:** Weekly, review and updates golden dataset (product owner). Daily, provides report of customers who didn't find a location (product owner).…
- **Shadow AI Audit (user-side):**
- **Agent Boundaries:**
- **Regulatory Exposure:** GDPR, Canada and California data privacy. Risk tier: limited. Controls: only connect necessary PII to book a reservation. ask for consent to collect PII..

→ Details: [`05-the-guardrails/`](05-the-guardrails/)

---

## The Pitch (M6)

**How you get this funded, shipped, and adopted.**

- **Horizon 1 (Now):**
- **Horizon 2 (Next):**
- **Horizon 3 (Bet):**
- **Board Narrative:** **The case:**
- **Ask:** ## M1 Baseline vs. Now
- **Key Strategic Change:**

→ Details: [`06-the-pitch/`](06-the-pitch/)
