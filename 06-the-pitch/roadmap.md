# AI Evaluation
### Bet Validation, Score: 2/5

* **Strengths:** Explicit recognition of the AI Value Archetype (Oracle) and an initial prototype URL indicates early experimentation is underway.
* **Gaps:** The bet is heavily reliant on internal conviction. No user interviews, workflow telemetry, or buyer evidence are cited. The kill criteria is defined strictly relative to cheaper competitors rather than an internal falsifiable business hypothesis or user adoption threshold.
* **Recommendation:** Formulate a falsifiable user hypothesis (e.g., *"80% of risk managers rely on automated risk scoring without manual correction in >85% of cases within 30 days"*) and test it in a 2-week pilot before building further.

### Capability Assessment, Score: 2/5

* **Strengths:** Clear decision to keep scope manageable by explicitly avoiding autonomous agentic architectures in this version.
* **Gaps:** Unclear data pipeline and ingestion setup for external/internal research. The reliance on third-party models without specified model routing, triage logic, or fallbacks creates major operational dependencies.
* **Recommendation:** Map out the exact data ingestion pipeline and establish a baseline model routing strategy (e.g., lightweight triage model for categorization, frontier model for complex risk synthesis) to quantify latency and API dependencies.

### Impact Analysis, Score: 2/5

* **Strengths:** Identifies a high-value domain (factory risk intelligence) where decision accuracy directly impacts supply chain operations.
* **Gaps:** Lacks specific quantified business metrics (e.g., target ARR expansion, hours saved per audit, or reduction in supply chain risk events). Opportunity costs against building adjacent operational workflow tools are unaddressed.
* **Recommendation:** Quantify the primary business metric—such as reducing manual research time per factory by 70% or driving a specific $X expansion in ACV—and track it against development costs.

### Defensibility Check, Score: 1/5

* **Strengths:** Accurately identifies Inspectorio as a top competitive encroachment threat.
* **Gaps:** Moat metrics and Data Flywheel scores are completely unpopulated. The "Recursive Learning" loop notes output compounding without defining how proprietary user feedback loops create network effects or proprietary dataset moats against incumbent platforms.
* **Recommendation:** Define a proprietary data flywheel—such as capturing non-public factory audit resolutions and human-in-the-loop (HITL) corrections—that competitors like Inspectorio cannot easily replicate via standard public data.

### Pricing Alignment, Score: 2/5

* **Strengths:** Anticipates a positive net margin shift (+12.2%).
* **Gaps:** Gross margins (current/AI-adjusted), unit COGS, pricing models (seat vs. usage/outcome), and break-even points are left blank. Seat-based pricing creates severe margin compression if power users run heavy external web-scraping and LLM research workflows (10x average volume).
* **Recommendation:** Transition from pure seat-based pricing to a hybrid model with a fixed base tier plus usage-based metering (e.g., credits per deep factory research report) to hedge against inference and scraping cost spikes.

### Trust & Reliability, Score: 1/5

* **Strengths:** Defines a concrete escalation trigger (Confidence < 90% triggers human review).
* **Gaps:** The Golden Dataset contains only 5 rows with no adversarial examples, making systematic accuracy or hallucination evaluations impossible. Failure mode coverage and HITL architecture details are completely missing.
* **Recommendation:** Expand the Golden Dataset to at least 100 benchmark cases including 20+ adversarial supply chain scenarios, and publish a structured error taxonomy for edge-case tracking.

### Governance & Scale, Score: 3/5

* **Strengths:** Solid compliance grounding with clear regulatory scope (EU AI Act, GDPR, SOC 2), explicit data minimization rules, no training on PII, and weekly PM audit cadences.
* **Gaps:** Unclear what technical infrastructure prevents cost or latency explosions at 10x scale. Shadow AI audit details and concrete agent boundaries are omitted.
* **Recommendation:** Automate the weekly audit process by logging human edit frequencies directly into a dashboard, triggering model re-prompting or fine-tuning when edit rates exceed 15%.

### Gap Identification, Score: 1/5

* **Strengths:** Proactively flags critical missing inputs across Moat, Margin, and Contract sections rather than assuming default stability.
* **Gaps:** Core strategy metrics across Margin and Moat modules are unpopulated template place-holders (`Module 1`, `Module 2`, blank numbers), leaving major blind spots for unit economics and competitive survival.
* **Recommendation:** Complete a formal stress-test of the unit economics and defensibility matrix before seeking board approval or scaling engineering resources.

---

### Overall Score: 1.9 / 5

### Biggest Risk

**Economic and defensibility collapse upon scaling:** Pursuing an "Oracle" archetype in a specialized vertical without populated unit economics (COGS/pricing) or a unique data flywheel leaves the product vulnerable to severe margin squeeze from usage spikes and fast replication by vertical incumbents like Inspectorio.

### Top 3 Actions

1. **Build a Robust Evaluation Dataset:** Scale the Golden Dataset from 5 rows to 100+ realistic/adversarial factory risk cases to baseline model precision and measure confidence scores objectively.
2. **Lock Down the Unit Economics & Pricing Strategy:** Calculate the total AI COGS per unit run and establish a hybrid/usage-based pricing model to protect margins against 10x power-user consumption.
3. **Formalize the Proprietary Data Flywheel:** Define how user edits ("Edit Category") and proprietary factory data feed directly into a fine-tuning or retrieval pipeline, transforming human corrections into a defensible moat.
_____


# Three-Horizon Roadmap & Board Pitch

Here is the strategic alignment, horizon classification, and kill criteria analysis for your backlog based on your **Factory Risk Intelligence** strategy.

### Horizon 1, Ship (0-4 weeks)

| Initiative | Strategy Component | Why it ships now | Confidence |
| --- | --- | --- | --- |
| 1. Agent searches RS team reference risk data | Bet | Essential core retrieval capability needed to power the base Factory Risk Intelligence prototype. | H |
| 2. Agent consolidates data and categorizes into signals | Bet | Directly delivers the primary automated value proposition of researching and categorizing evidence. | H |
| 3. Agent to map signal to company policy and explain “Why it matters” | Bet | Foundational functionality required to establish automated policy research and context generation. | H |
| 4. Human-in-the-loop: RS team reviews feedback and changes the mapping if disagree | Guardrails | Critical HITL feedback mechanism enabling weekly PM audit cadence and active oversight. | H |
| 5. Agent rates Risk Score of each information source specific to a factory | Bet | Core automated risk scoring feature defined directly in the main product workflow. | M |
| 9. RS Team reviews action items | Contract | Necessary human-in-the-loop validation layer for customer/operational safety triggers. | H |

---

### Horizon 2, Validate (1-3 months)

| Initiative | Strategy Component | Hypothesis | Kill Criteria | Confidence |
| --- | --- | --- | --- | --- |
| 6. Agent suggests an overall Risk Score of a factory | Bet | Synthesizing individual source scores into a factory-level score provides accurate, trusted risk assessment. | If overall risk score accuracy falls below 90% against golden dataset by week 6, we stop. | M |
| 7. Agent suggests action items | Contract | AI-suggested mitigation actions significantly accelerate RS team review times without sacrificing quality. | If RS team acceptance rate of suggested action items is under 60% by week 6, we stop. | M |

---

### Horizon 3, Explore (3-6 months)

| Initiative | Strategy Component | What must be true first | Confidence |
| --- | --- | --- | --- |
| 8. RS Team decides “Onboard Risk Action” according to the Risk Score | Guardrails | The agent's overall factory risk scoring and suggested actions must reach consistent >90% reliability. | L |

---

### Unmapped (cut or rethink)

| Initiative | Why it's unmapped | Recommendation |
| --- | --- | --- |
| 10. RS Team follow up | Standard operational task with no direct AI capability, strategy link, or feedback mechanism defined in M1–M5. | Cut from AI roadmap; manage via standard operational ticketing/CRM system. |

---

### Mapping Disagreements

No disagreements, all user mappings stand. *(Note: Since no explicit `[User-mapped to: X]` tags were included in the backlog list, all mappings above were established from scratch.)*

---

* **(a)** Horizon 1 is heavily over-indexed on core core feature development (Bet), leaving a gap in establishing clear unit economics or data flywheels (Margin & Moat) early on.
* **(b)** The single H3 bet to protect is **Initiative 8 (RS Team decides “Onboard Risk Action”)**, as automating onboarding decisions is the gateway to scaling full autonomous risk governance.
* **(c)** You should kill **Initiative 10 (RS Team follow up)** today, as it is a generic operational process that adds bloat to your AI product backlog without contributing to your strategy components.

---

### Strategic Summary Insights

* **(a) Horizon Distribution:** Your backlog is heavily over-indexed on **Horizon 1** (core extraction and UI workflow), leaving Horizon 3 thin with no long-term automated data flywheel or defensive moat experiments planned.
* **(b) Protected Bet:** Protect **Initiative 8 (RS Team decides "Onboard Risk Action" according to the Risk Score)** if budget is cut, as proving workflow-level action adoption is critical to establishing your product's operational moat.
* **(c) Initiative to Kill Today:** Kill **Initiative 10 (RS Team follow up)** immediately, as manual human task tracking adds no AI strategic value and distracts from core Oracle risk intelligence development.

_______
## Board Pitch

**Thesis (1 sentence):**
By automating multi-source factory audit analysis into standardized, policy-mapped risk scores, Factory Risk Intelligence cuts manual review overhead while expanding our portfolio risk coverage.

**The case:**
1. Why now: In the past 12 months, unstructured document processing and policy-mapping logic have reached production-grade accuracy, enabling us to eliminate manual data aggregation and eliminate human blind spots across diverse supplier networks.
2. What's defensible: Our moat relies on an intentional, standardized assessment framework across all factories that eliminates human bias; while incumbents like Inspectorio cover point-in-time inspections, our defensive edge is an uncompromised, objective risk baseline across heterogeneous data sources.
3. The economics: Net margin shift of +12.2%. Automated research and policy categorization drive unit economics that expand baseline gross margins while absorbing operational inference costs.

**The risks:**
1. Trust / failure modes: Misclassifying critical supplier violations could lead to severe supply chain disruptions or regulatory non-compliance; to prevent this, any confidence output below 60% or safety rubric flag triggers mandatory human-in-the-loop (HITL) review by the RS team before customer exposure.
2. Scale / governance: At 10x scale, excessive prompt context or frequent human edits could degrade system ROI; we enforce strict data minimization (EU AI Act/GDPR high-risk compliance, SOC 2 log controls) and weekly PM audits monitoring edit volume.
3. Competitive: If an existing market vendor provides the identical risk intelligence functionality at a lower total cost of ownership (including external platform/subscription fees), or if Horizon 2 overall risk score accuracy falls below 90% against our golden dataset by Week 6, we execute our kill criteria and pull the plug.

**The ask:**
2 Engineers and 1 Product Manager for a 1-Year horizon to ship Horizon 1 core retrieval/scoring capabilities and validate Horizon 2 overall factory scoring. Funding this requires pausing lower-ROI portfolio enhancements and deferring full autonomous onboarding features (Horizon 3) until reliability targets (>90%) are proven.
