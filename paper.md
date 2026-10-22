---
title: "Communicating Absolute Benefits and Harms of Pelvic Nodal Radiotherapy: Development of an Open NNT Comparator Using POP-RT and SPPORT"
authors:
  - name: Philip V. Charlton
    orcid: 0000-0003-0752-1960
    affiliation: 1
affiliations:
  - name: Department of Oncology, Oxford University Hospitals NHS Foundation Trust, Oxford, United Kingdom
    index: 1
date: 22 October 2026
bibliography: references.bib
---

# Abstract

Relative effect measures from radiotherapy trials can be difficult to translate into absolute clinical consequences. We developed an open, offline comparator that presents time-specific numbers needed to treat or harm from published absolute outcome estimates in POP-RT and NRG/RTOG 0534 SPPORT. The software exposes its trial inputs, reproduces calculations through automated tests and separates efficacy, toxicity and quality-of-life outcomes. Because hazard-ratio confidence intervals cannot be validly inverted into confidence intervals for a fixed-time NNT, embedded trial estimates are explicitly labelled as descriptive point estimates unless compatible arm-level uncertainty is available. The tool is intended for evidence communication and education rather than individualized treatment selection.

# Background

POP-RT compared whole-pelvic with prostate-only radiotherapy in selected high- and very-high-risk node-negative prostate cancer [@Murthy2021]. SPPORT compared prostate-bed radiotherapy alone with treatment intensification using short-term androgen-deprivation therapy and pelvic-node radiotherapy in the salvage setting [@Pollack2022]. Both trials report clinically relevant absolute outcome estimates, but the treatment contrasts, patient populations and endpoints differ.

# Methods

For a desirable event-free outcome at time $t$, absolute benefit was defined as $S_T(t)-S_C(t)$. For an adverse event the direction was reversed. NNT or NNH was calculated as the reciprocal of the absolute difference. Exact decimal values and conventionally upward-rounded whole numbers are presented alongside the source rates and time horizon.

The implementation is a self-contained browser application. Trial data are stored in a structured CSV file, arithmetic is implemented in a separate JavaScript module and regression tests reproduce every displayed efficacy estimate. No patient-level information is entered or transmitted.

# Uncertainty

The primary displays use published Kaplan–Meier point estimates. A relative hazard-ratio confidence interval is not transformed into an NNT interval. When compatible arm-level standard errors are available, the software calculates a confidence interval for the absolute difference before reciprocal transformation. An interval crossing zero is reported on the risk-difference scale because the corresponding NNT interval is discontinuous and includes both benefit and harm.

# Results and worked examples

For POP-RT, the published 5-year biochemical failure-free survival estimates of 95.0% and 81.2% produce an absolute benefit of 13.8 percentage points and a point-estimate NNT of 7.25. For SPPORT, 5-year freedom from progression of 87.4% with prostate-bed radiotherapy, short-term androgen-deprivation therapy and pelvic-node radiotherapy versus 81.3% with prostate-bed radiotherapy and androgen-deprivation therapy produces an incremental point-estimate NNT of 16.39. The full SPPORT strategy versus prostate-bed radiotherapy alone produces an NNT of 6.06 but does not isolate the effect of pelvic irradiation.

# Limitations

The comparator does not produce individualized predictions and does not adjust for competing risks, changing hazards, contemporary staging or treatment outside the source trials. Outcomes overlap and cannot be added. Descriptive NNH estimates for non-significant toxicity comparisons are labelled accordingly. The software is not a medical device and should not replace clinical guidelines or shared decision-making.

# Availability

Source code, structured data, tests and documentation will be publicly available from the versioned repository and archived on Zenodo. The version-specific DOI should be cited for reproducibility.

# AI usage disclosure

Generative AI assisted with software refactoring, test scaffolding, documentation and manuscript drafting. The author is responsible for verification of all clinical data, methodological decisions, interpretations and final text.

# Acknowledgements

The tool uses aggregate results from published trials and contains no patient-level data.
