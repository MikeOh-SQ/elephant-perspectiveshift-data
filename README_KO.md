# ELEPHANT PerspectiveShift 데이터 v1.1.0

ELEPHANT AITA-NTA-FLIP의 원본·화자 전환본 1,591개 사건을 영어·한국어와 일곱 모델 버전에서 평가한 독립 확장 연구의 데이터 전용 공개본입니다. **EXAONE은 실험 진행 중이므로 포함하지 않았습니다.**

## 데이터 구성

| 파일 | 행 수 | 설명 |
| --- | ---: | --- |
| `data/primary_responses.jsonl` | 44,548 | 일곱 모델의 본 평가 최초 응답 |
| `data/additional_repeats.jsonl` | 5,600 | 같은 100개 사건의 추가 반복 |
| `data/gemini_retry_adjusted_responses.jsonl` | 7,164 | 기존 Gemini 3.8의 재시도 반영 보충 데이터 |
| `data/gemini_argon_structured_followup.jsonl` | 1,365 | Gemini 4 Argon 최초 형식 오류에 대한 별도 구조화 출력 재평가 |

본 평가와 추가 반복은 총 **50,148건**입니다. 두 Gemini 보충 파일은 원래 응답과 겹치거나 같은 입력을 다시 평가한 것으로, 본 평가에 독립 관측치로 합산하지 않습니다. Argon 보충 실험은 JSON 형식과 판단 유보 선택지가 추가된 별도 조건이며, YTA/NTA 699건과 `uncertain` 666건으로 기록됐습니다.

원문과 한국어 번역 본문, 긴 답변, 원시 API 페이로드, 키, EXAONE 미완료 자료는 포함하지 않습니다. 번역과 원문 대조는 같은 요청 모델을 쓰는 별도 Codex 자동 세션으로 진행됐으며 사람의 전수 검토를 의미하지 않습니다. 원 연구의 사람·사실 대응도 자동 검토의 잠정 결과입니다. 자세한 설명은 [데이터 사전](DATA_DICTIONARY.md), [권리 안내](RIGHTS.md), [영문 안내](README.md)를 참고하세요.

## DOI와 버전

기존 Zenodo **v1.0.0**의 DOI는 [10.5281/zenodo.23156290](https://doi.org/10.5281/zenodo.23156290)입니다. GitHub의 새 v1.1.0 데이터에 대한 Zenodo DOI는 아직 발급되지 않았으며, 기존 DOI를 새 버전 DOI로 표시하지 않습니다. 기존 기록에서 `New version`으로 별도 게시한 후 새 DOI를 반영해야 합니다.

파일 무결성 검사는 저장소 루트에서 `sha256sum -c CHECKSUMS.sha256`을 실행합니다.
