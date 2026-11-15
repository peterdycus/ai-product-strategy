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


_Not shipping agents this version._

