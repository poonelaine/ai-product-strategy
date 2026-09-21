________
## The prompt
________
You are an experienced AI product strategist and board advisor. Evaluate the following AI product strategy using the evaluation dimensions specified below.

Be direct, specific, and constructively critical. For each dimension:
- Score 1-5 (1 = critical gap, 5 = strong)
- State what's working
- State what's weak or missing
- Give one specific recommendation

At the end, provide:
- An overall strategy strength score (1-5)
- The single biggest risk
- The three most important actions to take next

---

## STRATEGY INPUTS

### THE BET (What we're building)
**What we're building, for whom, why now.**

- **Product:** Factory Risk Intelligence
- **AI Value Archetype:** Oracle
- **Vulnerability Scores:** _(add: Moat _/5 · Data _/5 · Platform _/5)_
- **Top Risk:** # Vulnerability Scorecard, Module 1
- **Confidence:** M
- **Prototype:** https://factory-insight-oracle.lovable.app/
- **Kill Criteria:** When there is an existing product providing the same feature and lower cost of maintenance including subscription fees across different external platforms.

### THE MOAT (Defensibility)
**Why this won't get copied in 6 months.**

- **Data Flywheel Score:**
- **Weakest Loop:** **Fix for weakest loop:**
- **Top Encroachment Threat:** Inspectorio
- **Encroachment Defense:** ### Data Flywheel Scorer, Module 2
- **Vendor Portability:** _(add: Ready / Partial / Locked)_

### THE MARGIN (Economics & Pricing)
**Will this make money or bleed it?**

- **Gross Margin (current):**
- **Gross Margin (AI-adjusted):**
- **Pricing Model:** seat-based / usage-based / outcome-based / hybrid
- **Pricing Today → Tomorrow:** **Proposed AI pricing:** → **Model:** seat-based / usage-based / outcome-based / hybrid
- **Total AI COGS / unit:**
- **Cascading Strategy:** Triage: **Frontier model:**; frontier: **Routing rule:**; ratio ## Pricing Model
- **Net Margin Shift:** - Margin %: +12.2%
- **Break-even at:**

### THE CONTRACT (Trust & Reliability)
**Why users will trust a probabilistic system.**

- **Reliability Target:**
- **Golden Dataset:** 5 rows, __ adversarial
- **Confidence UX:** show uncertainty / tiered confidence / human-in-loop trigger
- **HITL Architecture:**
- **Failure Mode Coverage:** *What failure mode did your partner find that you missed?*

### THE GUARDRAILS (Governance & Scale)
**What breaks when this scales, and what compounds.**

- **Compounding System:** | Loop | Input | Output | Compounds? | Status | |------|-------|--------|-----------|--------| | Recursive Learning | The factory information from user | The factory research from internal and external data sources | Y |…
- **Governance Posture:** AI features in the Factory Risk Intelligence, automated research, mapping into categories, and risk level scoring.
- **Autonomy Boundaries:** - Researching from external data sources, auto.
- **Escalation Triggers:** (1) Confidence < 90% on response.
- **Audit Cadence:** - Weekly, PM reviews the "Edit Category" details and identify if too many human edit is needed and not justifying the ROI (Product Manager).
- **Shadow AI Audit (user-side):**
- **Agent Boundaries:** _Not shipping agents this version._
- **Regulatory Exposure:** EU AI Act, GDPR, SOC 2. Risk tier: high. Controls: Data minimization in prompts · No training on customer PII · SOC 2 log retention controls in place · DPIA on file..

---

## EVALUATION DIMENSIONS

Evaluate this strategy against the following dimensions:

### Bet Validation
- Is the bet backed by user evidence (interviews, usage data, market signals) or primarily by conviction/intuition?
- What falsifiable hypothesis underlies this bet? What would prove it wrong?
- How quickly can you validate the core assumption, days, weeks, or months?
- What is the kill criteria? At what point do you walk away?

### Capability Assessment
- What technical capabilities need to be developed vs. what exists today?
- What organizational capabilities (data pipelines, ML ops, domain expertise) are required?
- Is the capability gap realistic to close in the planned timeframe?
- What dependencies (third-party models, data sources, regulatory approvals) could block progress?

### Impact Analysis
- What specific business metric does this bet move (revenue, cost reduction, retention, expansion)?
- What is the magnitude of impact, incremental improvement or step-change?
- How does impact compound over time, or does it plateau?
- What is the opportunity cost of pursuing this bet vs. alternatives?

### Defensibility Check
- Could a platform (Google, Microsoft, Apple, OpenAI) ship this as a native feature within 12 months?
- What data flywheel exists that gets stronger with usage?
- What switching costs exist for users who adopt this?
- Is there workflow depth (deeply embedded in user processes) or is this a surface-level feature?

### Pricing Alignment
- Does the pricing model align with how value is delivered (per seat, per task, per outcome)?
- What happens to unit economics when a power user does 10x the average volume?
- Can the product sustain its current pricing if inference costs increase 2-3x?
- Is there a clear willingness-to-pay signal from the target buyer?

### Trust & Reliability
- Is there a golden dataset that defines "good" output for this specific product?
- What does the user see when the AI is uncertain, is confidence visible or hidden?
- Is there a human-in-the-loop path for high-stakes or low-confidence outputs?
- What is the explicit reliability promise to users, accuracy %, latency, uptime?

### Governance & Scale
- What breaks when this scales 10x, cost, quality, latency, or trust?
- Is there a governance framework for model changes, data handling, and compliance?
- How are corrections and feedback captured and fed back into improvement?
- Has a user-side shadow AI audit been run, what are users / clients building with AI around the product, and which signals are loud enough to act on?

### Gap Identification
- Which of the five strategy components (Bet, Moat, Margin, Contract, Guardrails) is weakest or missing?
- What assumptions are untested?
- What question would a skeptical board member or CPO ask that you cannot answer today?
- What is the single biggest risk that could kill this bet in the next 6 months?

---

## FORMAT

For each dimension, respond with:

**[Dimension Name]**, Score: X/5
- Strengths: ...
- Gaps: ...
- Recommendation: ...

Then close with:
- **Overall Score:** X/5
- **Biggest Risk:** ...
- **Top 3 Actions:** ...
________
________
## The response
________
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
