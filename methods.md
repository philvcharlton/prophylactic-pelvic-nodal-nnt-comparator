# Methods

For a desirable event-free outcome, the absolute benefit at time `t` is `S_treatment(t) - S_comparator(t)`. For an adverse event, the direction is reversed so that a positive difference denotes fewer adverse events with treatment. The exact reciprocal is reported in percentage-point form as `100 / |difference|`.

The interface displays the exact decimal estimate and the conventionally rounded whole-number result. Whole-number NNT/NNH is rounded upward because the quantity represents the minimum whole number of people who would need treatment for one additional outcome under the point estimate.

POP-RT and SPPORT address different clinical settings. The SPPORT full-strategy comparison combines short-term androgen-deprivation therapy and pelvic-node radiotherapy and therefore does not isolate the effect of pelvic irradiation.

All data used by the displayed examples are recorded in `data/trial_estimates.csv` with endpoint, time horizon, direction and source DOI.
