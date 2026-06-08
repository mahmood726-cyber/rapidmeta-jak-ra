# Data sources & provenance — JAK inhibitors / ACR20 / RA

All effect data are from peer-reviewed primary RCT reports and the corresponding
ClinicalTrials.gov results records. **No values are fabricated.** ACR20 responder
counts are derived as round(reported response % × analysed arm N), except
SELECT-NEXT where counts are reported directly.

| Trial | NCT | PMID | Reported ACR20 | Arm N (analysed) | Derived responders |
|---|---|---|---|---|---|
| ORAL Solo (tofacitinib 5 mg monotherapy, month 3) | NCT00814307 | 22873530 | 59.75% vs 26.67% (combined placebo) | 241 vs 120 | 144 vs 32 |
| RA-BEAM (baricitinib 4 mg + MTX, week 12) | NCT01710358 | 28199814 | 69.6% vs 40.2% | 487 vs 488 | 339 vs 196 |
| SELECT-NEXT (upadacitinib 15 mg + csDMARD, week 12) | NCT02675426 | 29908669 | 141/221 (64%) vs 79/221 (36%) — reported counts | 221 vs 221 | 141 vs 79 |
| FINCH 1 (filgotinib 200 mg + MTX, week 12) | NCT02889796 | 33504485 | 76.6% vs 49.9% | 475 vs 475 | 364 vs 237 |

Response percentages and analysed-arm denominators were retrieved from the
ClinicalTrials.gov v2 API outcome-measures records on 2026-06-08 and
cross-checked against each trial's primary publication abstract (Europe PMC).

## Pooled estimate (independent hand-check)
Random-effects (REML), log-odds-ratio inverse-variance:
- Pooled OR = **3.40 (95% CI 2.89 – 3.99)**
- Q(3) = 0.74 (p = 0.86) → I² = 0%, τ² = 0
- 95% prediction interval = 2.61 – 4.42

Per-trial odds ratios: ORAL Solo 4.08; RA-BEAM 3.41; SELECT-NEXT 3.17; FINCH 1 3.29.
