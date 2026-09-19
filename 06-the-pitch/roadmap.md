# Three-Horizon Roadmap & Board Pitch

Here is the strategic alignment, horizon classification, and kill criteria analysis for your backlog based on your **Factory Risk Intelligence** strategy.

### Horizon 1, Ship (0-4 weeks)

| Initiative | Strategy Component | Why it ships now | Confidence |
| --- | --- | --- | --- |
| **1. Agent searches RS team reference risk data** | Bet | Core foundational capability needed to deliver the Oracle archetype value proposition using internal reference data. | H |
| **2. Agent consolidates data and categorizes into signals** | Bet | Essential core data processing step required to structure raw research for risk intelligence analysis. | H |
| **3. Agent to map signal to company policy and explain “Why it matters”** | Bet | Primary AI value-add (Oracle archetype) providing automated contextual research and policy mapping directly from external/internal sources. | H |
| **4. Human-in-the-loop: RS team reviews feedback and changes the mapping if disagree** | Contract | Directly satisfies the primary HITL workflow, weekly audit cadence (PM tracking edits), and confidence escalation triggers. | H |

### Horizon 2, Validate (1-3 months)

| Initiative | Strategy Component | Hypothesis | Kill Criteria | Confidence |
| --- | --- | --- | --- | --- |
| **5. Agent rates Risk Score of each information source specific to a factory** | Guardrails | Rating source reliability improves overall score accuracy and reduces human intervention on weak sources. | If source rating accuracy does not achieve over 85% agreement with RS team audits by week 6, we stop. | M |
| **6. Agent suggests an overall Risk Score of a factory** | Margin | Automated overall scoring significantly reduces manual assessment time while maintaining acceptable risk posture. | If manual override rates on suggested risk scores exceed 20% by week 6, we stop. | M |
| **7. Agent suggests action items** | Margin | Moving from risk scoring to automated action suggestions drives user ROI and reduces end-to-end task duration. | If less than 60% of agent-suggested action items are accepted without major edits by week 6, we stop. | M |

### Horizon 3, Explore (3-6 months)

| Initiative | Strategy Component | What must be true first | Confidence |
| --- | --- | --- | --- |
| **8. RS Team decides “Onboard Risk Action” according to the Risk Score** | Moat | High baseline accuracy in overall risk scoring (Initiative 6) and stable human trust in system outputs must be proven first. | M |

### Unmapped (cut or rethink)

| Initiative | Why it's unmapped | Recommendation |
| --- | --- | --- |
| **9. RS Team reviews action items** | Standard manual operational step that contains no AI capability, flywheel loop, or unique risk/governance mechanism. | Cut from product engineering backlog; keep as standard internal SOP or handle natively via basic UI status workflow. |
| **10. RS Team follow up** | Generic human task management outside the core AI Oracle value proposition and systemic feedback loops. | Cut from core AI backlog; manage via standard task integration or external CRM/workflow tools. |

### Mapping Disagreements

No disagreements, all user mappings stand. *(Note: No explicit `[User-mapped to: X]` lines were present in the prompt input, so all items were mapped independently).*

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
