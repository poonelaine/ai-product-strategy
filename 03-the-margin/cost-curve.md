# Margin Calculator, Module 3

## Inputs
- Avg requests/user/month: 20
- Blended cost/request: $0.04
- Revenue/user/month: $10
- Non-AI COGS/user/month: $8

## Current Margin
- AI COGS/user: $0.80
- Total COGS/user: $8.80
- Gross margin: 12.0% ($1.20/user)

## Stress Test
| Scenario | AI COGS | Margin |
|----------|---------|--------|
| 3x Cost  | $2.40 | -4.0% ($-0.40) |
| 2x Usage | $1.60 | 4.0% ($0.40) |
##

# Build Your Cost Curve

## Features -> Tiers -> blended COGS
| Feature | Complexity | Model Tier | Cost/Req | Volume % | Weighted | Why the feature? |
|----------|---------|--------|----------|---------|--------|--------|
| Researching across 10+ internal and external data for a factory  | Simple | Small | $0.015 | 85% | $0.01275 |--------|
| Mapping the research results into company policy categories | Medium | Mid | $0.02 | 10% | $0.002 |--------|
| Rating a Risk Score and recommend action to onboard | Complex | Frontier | $0.04 | 5% | $0.002 |--------|
| Blended | | | | 100% | $0.01675 | |
##

# Pricing Strategy Block, Module 3

## Pricing Strategy
- Strategy posture: Skim
- Pricing model: Outcome / Resolution
- Unit of work metered: Research completed for a factory and recommend risk score
- Base fee ($/month): 10
- Price per unit: $0
- Estimated units/user/month: 20
- Implied revenue/user/month: $10.00

## Decision Note
Why this pricing structure fits the buyer and the value delivered: ·
##

# Cost Curve & Pricing Strategy

## Cost Model

| Cost Category | Per-User/Month | Notes |
|--------------|----------------|-------|
| Inference (primary model) | | |
| Inference (cascading/triage) | | |
| Infrastructure | | |
| Data/storage | | |
| Human-in-the-loop | | |
| **Total AI COGS** | | |

## Cascading Strategy
<!-- Cheap model → frontier model routing logic -->

**Triage model:**
**Frontier model:**
**Routing rule:**
**Expected cascade ratio:**

## Pricing Model

**Current pricing:**
**Proposed AI pricing:**
**Model:** seat-based / usage-based / outcome-based / hybrid

## Stress Tests

| Scenario | Impact on Margin | Response |
|----------|-----------------|----------|
| Inference costs 3x | | |
| Heaviest segment doubles | | |
| Model provider raises prices 50% | | |

## Board One-Pager
<!-- Before/After: Old SaaS revenue vs. AI usage revenue for your product -->

**Before (traditional SaaS):** 
- Revenue : $10 base / 12 months = $0.833
- COGS: $8 / 12 months = $0.66
- Gross Margin = 20.8% (+ $0.173)
- 
**After (AI-enabled):** 
- Revenue : $10 base + $0 x Outcome = $10
- COGS: $0.01675 x 20 times x 20 Users = $6.7
- Gross Margin = 33% (+ $3.3)

**Net margin shift:** 
- Margin %: +12.2%
- Gross $: + $3.28


