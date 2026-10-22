# Prophylactic Pelvic Nodal Irradiation—NNT Comparator

Version 1.4.0 is an offline, browser-based educational tool for comparing time-specific absolute benefits and harms reported in POP-RT and NRG/RTOG 0534 SPPORT.

## Use

Open `index.html` in a modern browser. No patient data are collected, transmitted or stored. The custom calculator accepts two rates at the same endpoint and time point. It reports the absolute difference and its reciprocal as NNT or NNH.

## Interpretation

The embedded trial estimates are population-level Kaplan–Meier point estimates. They are not individualized predictions. A hazard-ratio confidence interval cannot be inverted into a valid NNT interval. Version 1.4.0 therefore reports point-estimate NNTs for embedded trials and includes a tested uncertainty library for analyses where compatible arm-level standard errors or confidence intervals are available. See `docs/uncertainty.md`.

## Validation

Run:

```bash
npm test
```

The tests reproduce all displayed POP-RT and SPPORT calculations and cover equal rates, harm, invalid inputs, conventional rounding, positive NNT intervals and intervals crossing zero.

## Clinical-use boundary

This is research and education software, not a medical device or patient-specific decision-support system. It does not replace trial appraisal, current guidance, multidisciplinary assessment or shared decision-making.

## Citation

Use the citation shown by GitHub from `CITATION.cff`. After archival, cite the version-specific Zenodo DOI. Add the repository URL and DOI only after publication; see `PUBLISHING_CHECKLIST.md`.

## Licence

This repository is released under the MIT License. Third-party publications remain subject to their original terms.
