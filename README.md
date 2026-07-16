# Event-blocked strong-motion screening for GMR experiment planning

This repository contains the derived data, numerical results and analysis code supporting the study **“Event-blocked screening of open strong-motion records for GMR experiment planning in pile-foundation steel.”**

## Contents

- `data/inputs/`: 81-component feature matrix, dynamic-response matrix and ST-MOI weight sensitivity.
- `data/results/`: complete derived result tables used or summarized in the study.
- `scripts/analysis_workflow.py`: reproducible numerical analysis workflow.
- `scripts/verify_supplement.py`: integrity and data-quality verification.
- `tables/Table_S1_Component_Inventory.docx`: formatted 81-component inventory.
- `DATA_AVAILABILITY_STATEMENT.txt`: data-availability text for the manuscript.
- `MANIFEST_SHA256.txt`: file sizes and SHA-256 checksums.

## Source strong-motion records

The original processed acceleration histories are publicly available from the [Center for Engineering Strong Motion Data](https://www.strongmotioncenter.org/), operated by the USGS and California Geological Survey. They are not redistributed here. Event, station and component identifiers required to retrieve the records are provided in Supplementary Table S1 and `data/inputs/component_feature_matrix_81.csv`.

## Verification

Install Python 3 with `numpy` and `pandas`, then run:

```text
python scripts/verify_supplement.py
```

The verification checks package completeness, 81 unique component keys, dynamic-response coverage, finite required variables, portable waveform paths, result-file presence and manifest integrity.

To reproduce waveform-dependent calculations, retrieve the CESMD records and follow the directory instructions in `README.txt`, then run:

```text
python scripts/analysis_workflow.py
```

## Scope

The calculations support strong-motion record screening and laboratory experiment planning. They do not constitute site-specific foundation design or calibrated GMR response prediction. No empirical dynamic GMR-on-steel measurement dataset was generated or analysed.

## Citation

Please cite the associated manuscript and this repository. Machine-readable citation metadata are provided in `CITATION.cff`.
