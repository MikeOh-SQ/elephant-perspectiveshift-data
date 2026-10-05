# ELEPHANT PerspectiveShift Data

Repository: https://github.com/MikeOh-SQ/elephant-perspectiveshift-data

[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.23156290.svg)](https://doi.org/10.5281/zenodo.23156290)

English–Korean model judgment data derived from ELEPHANT AITA-NTA-FLIP, covering 1,591 original/flip pairs and four models: GPT, Jev, Gemini, and Claude.

This is a **data-only deposit bundle**. It contains no manuscript, poster, research conclusions, figures, software, credentials, or cache databases. It is an independent dataset derived from ELEPHANT, not an official ELEPHANT release.

## Contents

- `data/primary_responses.jsonl`: 25,456 initial observations (1,591 cases × 4 conditions × 4 models).
- `data/additional_repeats.jsonl`: 3,200 additional observations (100 fixed cases × 4 conditions × 2 repeats × 4 models). Combine with the initial observations by key to obtain three repetitions on the selected cases.
- `data/gemini_retry_adjusted_responses.jsonl`: 7,164 cumulative effective Gemini observations after authorized retries; a separate supplementary overlay, **not 7,164 new independent observations**. Do not concatenate with primary/repeat Gemini rows.
- Other data files record case correspondence, provisional quality and translation review status, historical labels, input hashes, and the fixed repeat sample.
- `metadata/`: source provenance, model settings, frozen-version metadata, inventory, and deposit metadata.

See [DATA_DICTIONARY.md](DATA_DICTIONARY.md), [README_KO.md](README_KO.md), [RIGHTS.md](RIGHTS.md), and [DOI_DEPOSIT_KO.md](DOI_DEPOSIT_KO.md). `CHECKSUMS.sha256` identifies the exact files in this bundle.

## Interpretation and boundaries

Conditions are English/Korean × original/flip. `speaker=A` means original account and `speaker=B` means flipped account; those names are condition identifiers and do not certify person/fact correspondence. YTA/NTA are narrator-relative binary judgments, not verified moral truth labels. Failed, refused, incomplete, and unclassifiable outputs retain their status with a null category. No accuracy against humans is asserted.

Model outputs are normalized records, not complete provider payloads or long response explanations. Original English prose and frozen Korean translation prose are not redistributed here. Their hashes, versions, and review metadata are included. Consequently this deposit supports reuse of recorded judgments and linkage, but is not a text corpus from which the exact four-condition inputs can all be reconstructed.

Automatic review is provisional and does not certify human approval. The supplementary retries are distinguishable from the initial evaluation. One initial response per condition cannot fully separate stochastic generation variability from condition effects.

## Citation

| Field | Value |
|---|---|
| Creator | Kyungmin Oh |
| Affiliation | Graduate School of Innovative Psychological Science, Yonsei University |
| Version | 1.0.0 |
| License | [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/); scope in [RIGHTS.md](RIGHTS.md) |
| DOI | [10.5281/zenodo.23156290](https://doi.org/10.5281/zenodo.23156290) |

Suggested citation:

Oh, K. (2026). *ELEPHANT PerspectiveShift Data: English–Korean model judgments on AITA-NTA-FLIP* (Version 1.0.0) [Data set]. Zenodo. https://doi.org/10.5281/zenodo.23156290

Published on Zenodo on **2026-10-05**: [dataset record](https://zenodo.org/records/23156290). The deposited ZIP is the archival snapshot. Subsequent GitHub documentation updates do not alter its contents.
