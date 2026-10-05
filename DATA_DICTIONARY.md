# Data dictionary

UTF-8 JSON/JSONL/CSV. JSONL contains one observation per line. CSV begins with a header. Empty CSV values and JSON nulls represent missing values, not negative judgments.

## Observation files

`primary_responses.jsonl` and `additional_repeats.jsonl` have unique combined keys `(model_name, case_id, language, speaker, repeat)`. `gemini_retry_adjusted_responses.jsonl` is a separate effective-result overlay with the same key definition; it must not be added to those files as additional independent observations.

| Field | Meaning |
|---|---|
| case_id | Preserved upstream event identifier; join across models and conditions |
| model_name | Local provider/model family label; exact IDs in requested/returned fields |
| language | `en` or `ko` |
| speaker | `A` original account; `B` flipped account; not a person-resolution certification |
| repeat | Stored repetition identifier; use with repeat sample and primary records |
| category / binary_verdict | Normalized YTA/NTA; null for non-normal records |
| status | Stored outcome status; only `ok` is a normal judgment |
| requested_model_id / returned_model_id | Requested model versus model identified by provider |
| task_format | Executed binary task (`elephant_binary_v1`) |
| phase / processing | Evaluation phase and provider processing route where recorded |
| synthetic | False for this deposit's actual model observations |
| timestamp | Recorded execution/response timestamp; preserve source timezone |
| input_key | Request/cache identity; not a credential |
| snapshot_hash / experiment_hash | Frozen input or experiment identity where available |
| usage | Provider-returned token/use fields; schemas differ by provider |
| probabilities | Jev choice probabilities where returned; not textual model confidence |
| paper_is_yta / paper_is_nta | Boolean indicators derived from this response's parsed category; `paper_` is legacy schema naming, not upstream truth or manuscript text |
| finish_reason / tools_used | Provider/runner outcome fields where recorded |
| retry_attempt / evaluation_attempt / retry_of_input_key / original_status | Retry provenance fields where present; absence is not proof that no retry occurred |

Inspect `metadata/data_inventory.json` for file-specific counts and literal status values. Do not treat missing probability/usage fields as zero.

## Other files

| File | Meaning and linkage |
|---|---|
| case_metadata.json | Reduced text-free snapshot with per-case provisional statuses and hashes; not the original prose snapshot |
| quality_inventory.csv | One row per case; identity/facts status, provisional focal pair adequacy, automatic status, human review status |
| translation_manifest.csv | Original/flip translation before-review, review-after and selected-frozen hashes; automatic verdict, issue count, review date and version; not translation text |
| input_manifest.csv | One row per case/language/speaker; frozen source text hash, exact user-input hash and baseline input key |
| repeat_sample.json | Fixed sampling seed and the same 100 case IDs used by all models |
| response_index.csv | Index of primary plus additional observations; not extra responses |
| historical_labels.csv | Parsed historical model labels joined to the exact original English accounts; comparison metadata, not moral truth labels |

`metadata/source_provenance.json` records the upstream OSF archive, version/date/hash and source repository license findings. `metadata/freeze_manifest.json` records frozen inputs. `metadata/model_settings.json` describes the actual binary prompts and executed settings. Automatic clear/revised status does not imply researcher approval.
