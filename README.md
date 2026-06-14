# RapidMeta — JAK Inhibitors for ACR20 Response in Rheumatoid Arthritis

**Living meta-analysis (RapidMeta dashboard).** A self-contained, offline-capable
interactive meta-analysis workbench: protocol, screening, editable extraction,
risk-of-bias, live re-pooling, a multi-panel statistics suite, GRADE, and PRISMA —
all client-side.

▶ **Live dashboard:** https://mahmood726-cyber.github.io/rapidmeta-jak-ra/

## Question
In adults with active rheumatoid arthritis, what are the odds of an **ACR20
response** (≥20% improvement in ACR criteria) with an oral **JAK inhibitor**
versus **placebo** (with or without background csDMARD), pooled across pivotal
phase-3 RCTs?

## Pooled result (random-effects, odds ratio)
| Metric | Value |
|---|---|
| **Pooled OR (ACR20, JAKi vs placebo)** | **3.40 (95% CI 2.89 – 3.99)** |
| Heterogeneity I² | 0.0% (Q(3) = 0.74, p = 0.86) |
| τ² | 0.000 |
| 95% prediction interval | 2.61 – 4.42 |
| Trials (k) | 4 | 
| Participants (analysed arms) | 2,728 |

Interpretation: across four phase-3 trials of four different JAK inhibitors,
ACR20 response is roughly **3.4× more likely** with a JAK inhibitor than with
placebo, with no detectable between-trial heterogeneity (I² = 0%).

## Trials included (real, published data)
ACR20 responder counts are taken from each trial's ClinicalTrials.gov results
record (response %) applied to the analysed arm size; SELECT-NEXT counts are
reported directly. See [`DATA_SOURCES.md`](DATA_SOURCES.md) for the full audit
trail (PMIDs, NCT IDs, percentages, denominators).

| Trial | NCT | Drug (dose) | Year | ACR20 timepoint | JAKi n/N | Placebo n/N |
|---|---|---|---|---|---|---|
| ORAL Solo | NCT00814307 | Tofacitinib 5 mg BID (mono) | 2012 | Month 3 | 144/241 | 32/120 |
| RA-BEAM | NCT01710358 | Baricitinib 4 mg + MTX | 2017 | Week 12 | 339/487 | 196/488 |
| SELECT-NEXT | NCT02675426 | Upadacitinib 15 mg + csDMARD | 2018 | Week 12 | 141/221 | 79/221 |
| FINCH 1 | NCT02889796 | Filgotinib 200 mg + MTX | 2021 | Week 12 | 364/475 | 237/475 |

## Methods note
- Effect measure: **odds ratio** from 2×2 event counts.
- Pooling: inverse-variance **random-effects** (REML τ²; DerSimonian–Laird
  cross-checked). I², Cochran's Q, Hartung–Knapp–Sidik–Jonkman adjusted CI, and a
  *t*-based 95% prediction interval (Cochrane Handbook v6.5) are reported in the
  dashboard's Statistics tab.
- Clinical heterogeneity: trials differ in background therapy (monotherapy vs
  MTX/csDMARD-add-on) and ACR20 timepoint (month 3 vs week 12); the dashboard
  retains per-trial and subgroup views.
- This is a **class-level** living synthesis (one pivotal trial per agent), not a
  drug-specific review; it is updated as new trials are added.

## Reproducibility
Built with the open [rapidmeta-kit](https://github.com/mahmood726-cyber/rapidmeta-kit)
generator from a ~30-line JSON config. The pooled numbers shown above were
reproduced independently by hand (log-OR inverse-variance) and match the
in-browser engine to the reported precision.

*Author: Dr Mahmood Ahmad. Not medical advice; for research/educational use.*
