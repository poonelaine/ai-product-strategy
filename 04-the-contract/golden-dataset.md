# Golden Dataset & Reliability Contract
## Golden Dataset, Module 4

Test cases:
  1. Edge: N · Judge: LLM, IN: Factory Name → OUT: A research of internal and external data sources
  2. Edge: N · Judge: LLM, IN: Factory Name → OUT: A summary into company policy category, with the source
  3. Edge: N · Judge: LLM, IN: Factory Name → OUT: A risk score of the Factory, comparing the same Manufacturing Type across the company Country of Production
  4. Edge: N · Judge: rule, IN: Factory Name → OUT: A benchmarking of the risk score, comparing to the median of other onboarded risk score
  5. Edge: Y · Judge: LLM, IN: Factory Name → OUT: No result found in external sources

Dataset health
- Total: 5
- Edge cases: 1 (20.0%)
- Judge mix: 20% rule / 80% LLM / 0% both

## Confidence UX Design

**Approach:** Tiered Confidence to show the source and allow adjustment of risk score

**Confident (>90%):** Full answer - mapping the source information into the company policy category, and provide a risk level contributing to the risk score

**Uncertain (50-90%):** Highlight result - suggest for human review when the source information is weak correlation to the company policy

**Not confident (<50%):** Show alert - ask for human input of risk level of a company policy category if there is missing information.

**User control surface:** 

Confidence threshold is controlled by Product Manager based on evaluation of the agent performance. Users can click and pop-up the reasoning. Users can adjust the Risk Level of each category, and the correction feedback to the model.

- Users see AI reasoning / drivers
- Users correct & override outputs
- Corrections feed back into the model / dataset
- Users adjust the confidence threshold _(not yet)_


## Reliability Contract

| Metric | Target | Measurement | Alert Threshold |
|--------|--------|-------------|-----------------|
| Accuracy | 90% | Weekly · 10 golden rows · LLM-as-Judge (accuracy rubric) | <88% → route to human review queue |
| Hallucination rate | <0% | Daily ·  LLM-as-Judge (flags fabricated policies/numbers) | >1% → auto-rollback to last good model |
| Latency (p95) | <2s | Continuous prod monitoring (Datadog) · p95 by endpoint | >3s for 30min → page on-call |
| Drift velocity | <0.5%/wk | 4-week rolling accuracy trend vs. golden dataset | >1% decay/wk → trigger gold-set audit |

## HITL Architecture

**Trigger:** Confidence <60% OR safety rubric flag fires on a customer-facing output

**Reviewer:** Rotating PM on call (weekday 9-5 ET) · senior CSM after hours

**Feedback loop:** Reviewer corrections feed back into the weekly gold-set audit. 5+ corrections in a week triggers a model retrain candidate.

