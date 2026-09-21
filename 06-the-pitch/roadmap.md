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

## Board Pitch

**Thesis (1 sentence):**
By automating factory risk research and policy compliance for our Risk Strategy team, Factory Risk Intelligence cuts manual risk assessment cycles while expanding our portfolio cover, locking in a +12.2% net margin shift before competitors like Inspectorio can capture our customer workflows.

**The case:**
1. Why now: Supply chain risk data has exploded across fragmented external platforms, forcing our Risk Strategy (RS) team into high-cost, manual aggregation rather than active risk mitigation; recent advances in LLM contextual extraction allow us to convert this unstructured web and reference data into instant, policy-mapped risk intelligence.
2. What's defensible: Our defensibility relies on an operational workflow moat; by embedding the RS team's human-in-the-loop review directly into policy mapping and action decisions, we create an internal feedback data loop that off-shelf point solutions like Inspectorio cannot replicate without access to our proprietary risk SOPs.
3. The economics: The unit economics demonstrate a +12.2% net margin expansion driven by automating manual research hours, backed by a dynamic routing strategy (triaging standard tasks to lower-cost models and reserving frontier models for complex policy mapping) to protect margins under volume spikes.

**The risks:**
1. Trust / failure modes: The primary disaster scenario is the system miscategorizing a critical factory compliance violation due to low source reliability, leading to unmitigated client exposure; we mitigate this by enforcing a hard human-in-the-loop escalation trigger whenever confidence drops below 90% and running weekly PM audit cadences on manual overrides.
2. Scale / governance: At 10x volume, cost bloat and model drift pose serious operational risks; we govern this under EU AI Act and GDPR high-risk controls using data minimization in prompts, no customer PII training, and a strict weekly PM edit-rate audit to kill unviable automation early.
3. Competitive: If incumbents like Inspectorio ship native automated policy mapping before our team adopts the workflow, or if manual override rates on our suggested risk scores exceed 20% in Horizon 2 testing, we trigger our kill criteria and halt investment.

**The ask:**
We are asking for 2 Engineers and 1 Product Manager for 1 Year to deliver Horizons 1 and 2 of Factory Risk Intelligence; to fund this, we will pause generic task management backlog items (Initiatives 9 and 10) and defer secondary workflow integrations to focus exclusively on core risk intelligence.
