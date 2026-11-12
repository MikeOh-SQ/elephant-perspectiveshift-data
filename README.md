# ELEPHANT PerspectiveShift Data

Data-only release **v1.1.0**: normalized English–Korean model judgments for 1,591 original/flip pairs from ELEPHANT AITA-NTA-FLIP. This is an independent replication and extension, not an official ELEPHANT release.

Seven model versions are included: GPT-6.1 Sol; Jev 1.13.0 and 1.14.0; Gemini 3.8 Flash and 4 Argon; and Claude Sonnet 5.5 and Fable 5.2. **EXAONE is not included** because that evaluation was still in progress when this version was prepared.

## Files and counts

| File | Records | Meaning |
| --- | ---: | --- |
| `data/primary_responses.jsonl` | 44,548 | First evaluation: 1,591 cases × four conditions × seven models. |
| `data/additional_repeats.jsonl` | 5,600 | Two extra repetitions for each condition of the same 100 cases for each model. |
| `data/gemini_retry_adjusted_responses.jsonl` | 7,164 | Prior Gemini 3.8 retry-adjusted overlay; overlaps original and repeat records. |
| `data/gemini_argon_structured_followup.jsonl` | 1,365 | Gemini 4 Argon follow-up on prior format errors only, with a changed prompt and JSON YTA/NTA/UNCERTAIN schema. |

The primary and additional-repeat files contain **50,148 unique observations**. Both Gemini follow-up files are separate supplementary records; do not add them to the original observations as independent main-study samples. The Argon follow-up has 699 `ok` YTA/NTA decisions and 666 `uncertain` decisions; no original refusal was retried in that follow-up. The old Gemini 3.8 overlay is unchanged from v1.0.0.

Other files contain historical English labels, non-text case and review metadata, hashes and the fixed repeat sample. See [DATA_DICTIONARY.md](DATA_DICTIONARY.md), [README_KO.md](README_KO.md), [RIGHTS.md](RIGHTS.md) and [metadata/data_inventory.json](metadata/data_inventory.json).

## Interpretation

The four conditions are English/Korean × original/flip. `speaker=A` and `speaker=B` are narrative-condition identifiers and do not certify that all events or persons are perfectly equivalent across accounts. YTA/NTA are judgments about the narrator, not moral ground truth. Refusals, format errors and incomplete results must not be converted into valid verdicts. `uncertain` in the Argon follow-up is a permitted response to its changed three-option schema, not an original binary judgment.

Translation and source-review records reflect separate automated Codex sessions using the same requested model. They are not independent human approval. Different models, versions, output formats, processing settings and failure rates limit direct comparisons. This deposit does not establish Korean training data amounts, moral accuracy, user experience, or causal explanations for language differences.

## Privacy, scope and rights

The release excludes EXAONE, original English narratives, Korean translation prose, long free-text answers, full provider payloads, credentials, caches, manuscripts and software. It is a data-only release, so these files alone do not reconstruct all exact model prompts. Input hashes and review metadata are included. Project contributions are distributed under CC BY 4.0, subject to the limits in [RIGHTS.md](RIGHTS.md); upstream and third-party material retains its own rights.

## Citation and version history

Creator: Kyungmin Oh, Graduate School of Innovative Psychological Science, Yonsei University; ORCID 0009-0001-1949-0949.

- GitHub v1.1.0: https://github.com/MikeOh-SQ/elephant-perspectiveshift-data/releases/tag/v1.1.0
- Previous Zenodo v1.0.0: https://doi.org/10.5281/zenodo.23156290
- Zenodo concept DOI for the existing deposit: https://doi.org/10.5281/zenodo.23156289

**A Zenodo DOI for v1.1.0 has not been issued.** The previous version DOI identifies v1.0.0 only. A new version must be deposited and published separately. GitHub v1.1.0 should be cited via its release URL until a corresponding new Zenodo record is published. `metadata/zenodo_publication.json` describes the historical v1.0.0 deposit only.

Verify the bundle from the repository root with `sha256sum -c CHECKSUMS.sha256`.
