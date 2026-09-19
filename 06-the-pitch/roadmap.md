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
