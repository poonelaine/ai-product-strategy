# Compounding System Design

## Feedback Loops

| Loop | Input | Output | Compounds? | Status |
|------|-------|--------|-----------|--------|
| Recursive Learning | The factory information from user | The factory research from internal and external data sources | Y | missing |
| Cross-Domain Transfer | The factory names in progress of onboarding audit | Suggested action to approve or decline | Y | missing |
| Network Intelligence | The factory audit history if it is an existing factory to other vendor | Factory audit status from other vendor | N | missing |

**Broken loop identified by partner:** Recursive learning

**Fix plan:** Add an edit function, to allow mapping of the evidence into other Policy Category

## Context Connectivity
<!-- How does knowledge flow across teams and domains? Where does it silo? -->

**How knowledge flows:** Edit report - to be reviewed by product team and determine action to modeling 

**Where it silos:** Limited persona - Few users may edit with different perspectives back and forth 



## Governance Policy

<!-- Governance Policy, Factory Risk Intelligence v 1.0 -->


**Scope:** AI features in the Factory Risk Intelligence, automated research, mapping into categories, and risk level scoring. 
- Excludes: Onboarding workflow and features which are covered by another internal manufacturing visibility system.

**Autonomy boundaries:** 
- Researching from external data sources, auto.
- Researching from internal factory audit history, auto.
- Categorizing evidence according to company policy, auto.
- Rating a risk score according to the evidence, auto.
- Suggesting the action to Approve or Decline the factory to onboard, human approval required.
- Feedinhg the final decision into onboarding process system, never auto.

**Escalation triggers:** 

(1) Confidence < 90% on response.

(2) User flagged thumbs down

(3) User edit the mapping more than one evidence per policy category

(4) User edit the action item from Approve to Decline

(5) More than three searches for the same factory and vendor information

**Audit cadence:** 
- Weekly, PM reviews the "Edit Category" details and identify if too many human edit is needed and not justifying the ROI (Product Manager).
- Monthly, PE reviews summary of "Edit Category" + "Thumbs Down" and advise any recursive learning to the model, or human-in-loop action is required (Product Engineer).
- Quarterly, Business stakeholder reviews the usage and summary of decision suggested and action approved by human, to sign-off ROI actualized (Managing Director and DIrector).

**Regulatory exposure (EU AI Act / other):** EU AI Act, GDPR, SOC 2. Risk tier: high. Controls: Data minimization in prompts · No training on customer PII · SOC 2 log retention controls in place · DPIA on file..


## Agent Topology

_Not shipping agents this version._


# Shadow AI Audit (user-side), Module 5

## Discover, User-Side Workarounds

| Workaround | Signal Source | Signal Type| Freq | Spend: $/mo | Decision |
|------|-------|--------|-----------|--------|--------|
| Export summary report of researches done in certain period | source: Support ticket | signal: Workflow gap | freq: L | spend: $20/mo | decision: Build |
| Pipe API output to onboarding system to skip human approval | source: User interview | signal: Capability gap | freq: L | spend: $20/mo | decision: Partner |
| Users expect researches for factory in non-English country | source: User interview | signal: Capability gap | freq: L | spend: $20/mo | decision: Partner |
| Users run the agent to probe other risk domains to assess onboarding | source: Support ticket | signal: Pricing gap | freq: H | spend: $20/mo | decision: Ignore |
| Users run on off-the-shelf agent to compare the research result of our agent | source: Other | signal: Trust gap | freq: M | spend: $0/mo | decision: TBD |

## Pattern Assessment
- Workarounds found: 5
- Build candidates: 1
- Partner candidates: 2
- Ignore decisions: 1
- Adjacent spend: $80/mo
- Dominant signal: Capability gap

## Action Plan
### Build
(1) Build Summary report - provide CSV export to support audit cadence,turn ad-hoc ask into one of the agent's business value in operation workflow and justifying ROI
CS onboarding domain enrichment (high freq, internal workflow)

### Partner
(2) Partner with manufacturing visibility system product team to enable API integration - build new capability to automate final human approved decision into the existing onboarding processes.

(3) Partner with Business stakeholder in global offices - increase research coverage from localized sources, build Translation capability into English.

### Ignore + Monitor
(4) Ignore Users running our agent for out of scope Domain - not in our current product vision, strategy and roadmap. Monitor if any increasing sentiment and pitch to relative Business leader to absorb strategically.

(5) TBD discovery work to identify capability and confidence gap between the off-the-shelf tool and our agent.

## Roadmap Brief
Based on your audit: 5 user-side workarounds discovered.

Decisions: 1 build · 2 partner · 1 ignore · 1 TBD.

Estimated adjacent spend: $80/mo across surveyed users.

Dominant signal: Capability gap.

Recommended next step: Capability gaps dominate, users want something your product does not do. Strongest near-term move is building one or two of these natively before a competitor does.

Sequence the Build column by frequency × strategic relevance. Confirm Partner candidates with the external tools' partnership teams. Re-run this audit each quarter, workarounds shift fast.

