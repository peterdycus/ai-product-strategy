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

**Approach:** show uncertainty / tiered confidence / human-in-loop trigger

**High confidence (>90%):**
**Medium confidence (70-90%):**
**Low confidence (<70%):**

**User control surface:**

## Reliability Contract

| Metric | Target | Measurement | Alert Threshold |
|--------|--------|-------------|-----------------|
| Accuracy | | | |
| Hallucination rate | | | |
| Latency (p95) | | | |
| Drift velocity | | | |

## HITL Architecture
<!-- When does a human step in? What's the escalation path? -->

## Red-Team Findings
*What failure mode did your partner find that you missed?*
