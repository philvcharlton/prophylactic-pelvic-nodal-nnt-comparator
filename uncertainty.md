# Uncertainty policy

## Embedded trial estimates

The embedded NNT and NNH values are descriptive reciprocals of published absolute differences at specified time points. They are not confidence limits and should not be interpreted as individualized treatment effects.

Hazard ratios summarize relative time-to-event effects over follow-up. Their confidence intervals cannot be inverted to obtain confidence intervals for an NNT at a fixed time. Where the publications do not provide compatible arm-level uncertainty for the survival probabilities or their difference, the software deliberately reports no NNT confidence interval.

## Supported calculation

When compatible arm-level standard errors are available, the library computes the risk-difference standard error for independent randomized arms:

`SE(RD) = sqrt(SE_treatment^2 + SE_comparator^2)`

and a two-sided 95% normal interval. If only arm-level 95% confidence limits are available, the software can approximate each standard error from the interval width. This assumes symmetric normal intervals and must be labelled approximate.

If the risk-difference interval is wholly beneficial, its endpoints are reciprocally transformed to an NNT interval. If wholly harmful, they are transformed to an NNH interval. If the interval crosses zero, the NNT scale is discontinuous; the software returns the risk-difference interval and states that both benefit and harm remain compatible with the data.

## Reporting rules

- Report endpoint and time horizon beside every NNT/NNH.
- Report the underlying arm rates and absolute difference.
- Separate benefit and toxicity outcomes.
- Mark non-significant NNH values as descriptive.
- Never derive an NNT interval from a hazard-ratio interval.
- Label reconstructed Kaplan–Meier or pseudo-individual-participant analyses as reconstructed.
- Do not combine overlapping outcomes into a composite net benefit.
