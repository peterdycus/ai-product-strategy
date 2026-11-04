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
