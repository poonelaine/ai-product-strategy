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
- (1) Confidence < 90% on response.
- (2) User flagged thumbs down
- (3) User edit the mapping more than one evidence per policy category
- (4) User edit the action item from Approve to Decline
- (5) More than three searches for the same factory and vendor information

**Audit cadence:** 
- Weekly, PM reviews the "Edit Category" details and identify if too many human edit is needed and not justifying the ROI (Product Manager).
- Monthly, PE reviews summary of "Edit Category" + "Thumbs Down" and advise any recursive learning to the model, or human-in-loop action is required (Product Engineer).
- Quarterly, Business stakeholder reviews the usage and summary of decision suggested and action approved by human, to sign-off ROI actualized (Managing Director and DIrector).

**Regulatory exposure (EU AI Act / other):** EU AI Act, GDPR, SOC 2. Risk tier: high. Controls: Data minimization in prompts · No training on customer PII · SOC 2 log retention controls in place · DPIA on file..


## Agent Topology

_Not shipping agents this version._




## Shadow AI Audit

| Tool | Owner | Risk Level | Decision |
|------|-------|-----------|----------|
| | | H / M / L | keep / govern / kill |
| | | H / M / L | keep / govern / kill |
| | | H / M / L | keep / govern / kill |

**Total tools found:**
**Tools after triage:**
**Estimated hidden spend:**
