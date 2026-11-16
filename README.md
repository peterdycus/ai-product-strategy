# Enterprise.com IA Bot to book rental vechicles

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

The Prototype Bet

What I Built

A product that allows the customer to use a AI agent to reserve a rental car.

Tool Used

Lovable

Prototype Link

(https://roam-and-reserve-ai.lovable.app)

AI Value Archetype

Copilot

The Bet in One Sentence

Some customers will prefer to use an AI agent to find and book the right rental vechicle for their needs.

Kill Criteria

If adoption is below 20% in first four months, kill or pivot.

→ Details: [`01-the-bet/`](01-the-bet/)

---

## The Moat (M2)

**Why this won't get copied in 6 months.**

# Data Flywheel Map

> Score each loop 1-5. Your weakest loop is where competitors attack first.
> The four loops below are the M2 starting point - adapt if your product has 2 or 6 loops instead of 4.

## Flywheel Loops

| Loop | What It Measures | Score 1 | Score 5 | Score |
|------|------------------|---------|---------|-------|
| **Correction** | Do users fix AI outputs? Is that signal captured and reused? | No capture | Automated retraining | __/5 |
| **Preference** | Does the product learn individual / team preferences over time? | Stateless | Deep personalization | __/5 |
| **Domain Context** | Does usage in one area improve quality in adjacent areas? | Siloed | Cross-domain transfer | __/5 |
| **Network** | Does each new user / team make the product better for everyone? | Isolated | Strong network effects | __/5 |

### Correction Loop - 2/5
**What you capture today:**
**How it compounds:**

### Preference Loop - 2/5
**What you capture today:**
**How it compounds:**

### Domain Context Loop -3/5
**What you capture today:**
**How it compounds:**

### Network Loop - 4/5
**What you capture today:**
**How it compounds:**

**Total Flywheel Score: 10/20**
**Weakest Loop:** Correction Lop
**Fix for weakest loop:**

---

## Encroachment Threat Assessment

### 1. Platform Encroachment
**Attacker:** Muse 
**Vector:** Able to add to it platform easily. May put competitors first.   
**Time-to-threat:** 1 years 
**% of value at risk:** 50%

### 2. Vertical Competitor
**Attacker:** Hertz 
**Vector:** Can create their proprietary IA reservation creator. Can take away some marketshare over time. 
**Time-to-threat:** 2 years
**% of value at risk:** 50%

### 3. Adjacent Expansion
**Attacker:** Expedia 
**Vector:** Can create their proprietary IA reservation creator. May put competitors first. 
**Time-to-threat:** 2 years
**% of value at risk:** 50%


## 90-Day Encroachment Plan

*Your partner played the Big Tech attacker. What was their plan to kill you?*

**Attacker:**
**Attack vector (target the weakest loop):** Correction Loop 
**Weeks 1-4 - what they ship:** Improve users being able to correct responses. 
**Weeks 5-8 - how they poach users:** loyal points for using the AI reservation creator 
**Weeks 9-12 - why users don't come back:** improve the preference loop 
**Your defense:** Making the product more customizable and personalized will increase repeat usage and rental bookings.


---

## 90-Day Encroachment Plan

*Your partner played the Big Tech attacker. What was their plan to kill you?*

**Attacker:**
**Attack vector (target the weakest loop):** Correction Loop 
**Weeks 1-4 - what they ship:** Improve users being able to correct responses. 
**Weeks 5-8 - how they poach users:** loyal points for using the AI reservation creator 
**Weeks 9-12 - why users don't come back:** improve the preference loop 
**Your defense:** Making the product more customizable and personalized will increase repeat usage and rental bookings.


→ Details: [`02-the-moat/`](02-the-moat/)

---

## The Margin (M3)


## Inputs
- Avg requests/user/month: 40000
- Blended cost/request: $0.02
- Revenue/user/month: $750
- Non-AI COGS/user/month: $5

## Current Margin
- AI COGS/user: $800.00
- Total COGS/user: $805.00
- Gross margin: -7.3% ($-55.00/user)

## Stress Test
| Scenario | AI COGS | Margin |
|----------|---------|--------|
| 3x Cost  | $2400.00 | -220.7% ($-1655.00) |
| 2x Usage | $1600.00 | -114.0% ($-855.00) |


Pricing Strategy Block, Module 3

Pricing Strategy
- Strategy posture: Penetrate
- Pricing model: Hybrid (base + usage)
- Unit of work metered: vechical rental booked
- Base fee ($/month): 0
- Price per unit: $0
- Estimated units/user/month: 0
- Implied revenue/user/month: $0.00

---

## The Contract (M4)

**Why users will trust a probabilistic system.**


# Golden Dataset & Reliability Contract

## Golden Dataset Spec
Golden Dataset, Module 4

Test cases:
  1. Edge: N · Judge: both, IN: Provides location  for rental → OUT: Provide rental locations closest to users location
  2. Edge: N · Judge: both, IN: requesets a SUV  → OUT: Provide users with list of SUV and ask where are you going?
  3. Edge: N · Judge: both, IN: provides number of passengers  → OUT: provide list of vechicles that match number of passengers
  4. Edge: N · Judge: both, IN: Customer ask for pricing → OUT: provide vechile types for user to select from
  5. Edge: N · Judge: both, IN: Customer select a vehicle  → OUT: Ask for what locations they'd like to pick up
  6. Edge: N · Judge: both, IN: Customer has chosen a vehicle and location → OUT: ask for date of the rental
  7. Edge: N · Judge: both, IN: Customer provides data of the rental and where they're going → OUT: Provide locations to pick up the rental
  8. Edge: N · Judge: both, IN: Customer has selected a vehicle, location and date → OUT: Provide list of options for the rental and ask them to select them
  9. Edge: N · Judge: both, IN: Customer has selected  a vehicle, location and provideded dates → OUT: Ask if the user is ready to review the rental agreement
  10. Edge: Y · Judge: both, IN: Customer provide a partial location → OUT: ask for customer provide additional details 

Dataset health
- Total: 10
- Edge cases: 1 (10.0%)
- Judge mix: 0% rule / 0% LLM / 100% both

**Adversarial rows included:** __
**Coverage gaps identified by partner:**

## Confidence UX Design

## Confidence UX Design

**Approach:** Tiered confidence with human-in-loop when not confident <50%

**Confident (>90%):** provides full answer and show process that led to full example. user is prompted to answer the next question and/or accept, reject request

**Uncertain (50-90%):** Soften the language and ask for additional details improve the confidence.

**Not confident (<50%):** Unable to generate answer with confidence. Connect with a human to help the customer.

**User control surface:** 

- Users adjust the confidence threshold
- Users see AI reasoning / drivers
- Corrections feed back into the model / dataset
- Users correct & override outputs _(not yet)_


## Reliability Contract

## Reliability Contract

| Metric | Target | Measurement | Alert Threshold |
|--------|--------|-------------|-----------------|
| Accuracy | 90% | Weekly evaluation of golden rows. uses LLM as judges. HITL if below 85%. | 85% → route to human review queue |
| Hallucination rate | <1% | Same weekly run of golden rows. If hallicination rate is lower than 2% roll back. | >2% → auto-rollback to last good model |
| Latency (p95) | <500 ms | Continuous monitor data log. | >1200 ms → auto-rollback to last good model |
| Drift velocity | <0.5%/4w | Evaluate on a rolling four week cycle. If drift is lower that 1%. Gold-set audit. | >1%/4W investigate → trigger gold-set audit |

## HITL Architecture

**Trigger:** Confidence is less than 50%

**Reviewer:** PM or Engineer

**Feedback loop:** The PM or Engineer corrects the issue identified in the evaluation findings. This could be update the golden data set.


## HITL Architecture
<!-- When does a human step in? What's the escalation path? -->

## Red-Team Findings
*What failure mode did your partner find that you missed?*


→ Details: [`04-the-contract/`](04-the-contract/)

---

## The Guardrails (M5)

**What breaks when this scales, and what compounds.**

# Compounding System Design

## Feedback Loops

| Loop | Input | Output | Compounds? | Status |
|------|-------|--------|-----------|--------|
| Recursive Learning | user corrects a location | learns and modifies the location | Y | broken |
| Cross-Domain Transfer | user corrects a vehicle  type | saves vehicle type is added  in user preference | N | broken |
| Network Intelligence | user corrects a location | location data is put in alert queue to fix or investigate | N | active |

**Broken loop identified by partner:** Recursive Learning may end up creating an inaccurate location 
**Fix plan:** When the location is correct by the user and does match the golden data set, send an alert to investigate. 

## Context Connectivity
<!-- How does knowledge flow across teams and domains? Where does it silo? -->

**How knowledge flows:** IA chat location > Alerts queue 

**Where it silos:** location and vehicle data storage in user preferences 


## Governance Policy

**Scope:** booking of rental vechicle Excludes: customer service requests

**Autonomy boundaries:** customer service request are sent to customer service, auto. user can't find their rental, human approval required. rentals not available in their location, human approval required.

**Escalation triggers:** 1. confidence is <70% on finding a rental at the location 2. confidence is <70% on finding a location 3. customer message is asking for help with a technical issue or loyalty question it gets flagged and sent to customer service 4. customer isn't able to find a location or a rental at location, a human will intervene

**Audit cadence:** Weekly, review and updates golden dataset (product owner). Daily, provides report of customers who didn't find a location (product owner). Monthly, review systems issues and determine optimizations to put into place (product owner).

**Regulatory exposure (EU AI Act / other):** GDPR, Canada and California data privacy. Risk tier: limited. Controls: only connect necessary PII to book a reservation. ask for consent to collect PII..

## Agent Topology
<!-- If using agents: what can each agent do? What can't it do? Who approves what? -->

## Shadow AI Audit

Shadow AI Audit (user-side), Module 5

## Discover, User-Side Workarounds
- user wants to be picked up | source: Support ticket | signal: Workflow gap | freq: L | spend: $0/mo | decision: Partner
- user wants adaptive equipment | source: Support ticket | signal: Workflow gap | freq: L | spend: $0/mo | decision: Build
- user has feeback on their experience  | source: Support ticket | signal: Workflow gap | freq: L | spend: $0/mo | decision: Partner

## Pattern Assessment
- Workarounds found: 3
- Build candidates: 1
- Partner candidates: 2
- Ignore decisions: 0
- Adjacent spend: $0/mo
- Dominant signal: Workflow gap

## Action Plan
### Build
user wants adaptive equipment

### Partner
user wants to be picked up and  has feedback 

### Ignore + Monitor
None 

## Roadmap Brief
Based on your audit: 3 user-side workarounds discovered.
Decisions: 1 build · 2 partner · 0 ignore · 0 TBD.
Estimated adjacent spend: $0/mo across surveyed users.
Dominant signal: Workflow gap.

Recommended next step: Workflow gaps dominate, your users are stitching your product into multi-step pipelines. Strongest near-term move is partner integrations with the AI tools they already chain in.

Sequence the Build column by frequency × strategic relevance. Confirm Partner candidates with the external tools' partnership teams. Re-run this audit each quarter, workarounds shift fast.
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
