# Example: SaaS startup weekly metrics with an activation drop

## Scenario
A seed-stage SaaS founder pastes Monday morning dashboard numbers before the weekly team sync. Several metrics moved significantly.

## Input
- **Metric export**: "Week of March 16-22, 2026: New signups: 142 (prev: 118). Activation rate (completed onboarding): 31% (prev: 38%). MRR: $18,200 (prev: $16,800). Churn: 2 accounts ($450 MRR, prev: 1 account $200). Demo requests: 23 (prev: 14). Support tickets: 47 (prev: 31). NPS: 42 (prev: 45)."
- **Primary KPIs**: "MRR, activation rate, demo requests, churn."

## Expected output
**Weekly Metrics Summary — March 16-22, 2026**

**Highlights**
| Metric | This week | Last week | Delta |
|--------|-----------|-----------|-------|
| MRR | $18,200 | $16,800 | +8.3% |
| Activation rate | 31% | 38% | -7 points (-18.4%) |
| Demo requests | 23 | 14 | +64.3% |
| Churn | 2 accounts ($450) | 1 account ($200) | +100% accounts, +125% MRR |

**Outliers**
- Activation rate dropped 7 points (31% vs 38%), a relative drop of 18.4%.
- Demo requests rose 64.3% (23 vs 14). The source is not in the export, so it needs attribution.
- Support tickets spiked 51.6% (47 vs 31) — may be correlated with the activation drop.
- New signups rose 20.3% (142 vs 118).
- Churn went from 1 account ($200) to 2 accounts ($450). Counts this small overstate the change, but it is past the 15% line.

**Likely drivers**
- Signup volume increased 20%, which may be pulling in lower-intent users and dragging activation down.
- If anything changed in onboarding this week, that is the first place to look for the activation dip. The export does not say whether anything did.
- Churn increase is small in absolute terms ($450) but the account count doubling (and churned MRR up 125%) warrants a look at the two accounts.

**Questions for the team**
1. Did anything change in onboarding this week, and what does the step-by-step drop-off look like?
2. What source drove the demo request spike — is it the same channel as the signup increase?
3. Are the 47 support tickets related to onboarding issues, or is this a separate trend?

**Overall health**: MRR growth is strong but the activation drop is a leading indicator that needs investigation before the team acts on the signup growth.

## Why this is a good result
The summary separates signal from noise, connects related metrics (signups up + activation down), and gives the team specific questions instead of generic commentary.