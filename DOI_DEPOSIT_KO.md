# 데이터셋 DOI 등록 안내

권장 방식은 이 데이터 폴더의 ZIP을 **Zenodo에 직접 데이터셋으로 등록**하고, 새 GitHub 저장소는 동일 자료의 탐색·다운로드 창구로 사용하는 것입니다. 논문을 공개할 필요는 없습니다. GitHub 저장소 주소 자체가 DOI는 아닙니다.

1. 저자 **Kyungmin Oh**, 이용허락 **CC BY 4.0**을 메타데이터에 반영했습니다. Zenodo 이름 필드는 `Oh, Kyungmin`(성, 이름)으로 기록했습니다. 소속은 **Graduate School of Innovative Psychological Science, Yonsei University**입니다. Zenodo 공개 저자 정보에서 확인한 ORCID는 **0009-0001-1949-0949**입니다. `.zenodo.json`과 `metadata/deposit_metadata_draft.json`에 같은 정보를 넣었습니다. 공개용 버전은 **1.0.0**으로 준비했습니다. 공개 시점을 정합니다. 데이터 저장소: https://github.com/MikeOh-SQ/elephant-perspectiveshift-data.
2. 데이터 전용 GitHub 저장소는 `MikeOh-SQ/elephant-perspectiveshift-data`입니다. 현재 공개(Public) 상태입니다. 이 폴더의 파일만 사용합니다. 기존 연구 저장소의 `.git`이나 이력을 복사하지 않습니다. 기존 비공개 저장소의 논문·소스는 옮기지 않습니다.
3. Zenodo에서 새 업로드를 만들고 자료 유형을 **Dataset**으로 선택합니다. ZIP, 제목, 설명, 저자, 버전과 이용 조건을 입력합니다.
4. DOI 항목에서 기존 DOI가 없음을 선택하고 **Get a DOI now!**로 DOI를 예약할 수 있습니다. 예약과 공개·등록 완료는 서로 다릅니다. 예약한 DOI를 논문 및 데이터 인용에 사용할 수 있도록 기록합니다.
5. 예약 DOI와 새 저장소 주소를 자료 설명에 반영한 최종 파일로 교체하고 체크섬도 갱신합니다. 내용과 공개 범위를 확인한 뒤 Zenodo에서 Publish합니다. 공개된 데이터셋의 버전 DOI를 논문에 인용합니다.
6. 새 GitHub README에 해당 데이터 DOI 링크를 추가합니다. GitHub와 Zenodo에 같은 데이터 버전을 제공하고, 수정은 새 버전으로 구분합니다.

## 인용 서식

`Oh, K. ([공개 연도]). ELEPHANT PerspectiveShift Data: English–Korean model judgments on AITA-NTA-FLIP (Version 1.0.0) [Data set]. Zenodo. https://doi.org/10.5281/zenodo.23156290`

위 문구는 서식 예시입니다. 아직 발급받지 않은 DOI나 확정되지 않은 공개 연도를 실제 인용으로 사용하지 않습니다. 발표 논문 DOI와 데이터 DOI는 별개입니다.

## 공식 안내

- DOI 예약: https://help.zenodo.org/docs/deposit/describe-records/reserve-doi/
- 업로드: https://help.zenodo.org/docs/get-started/quickstart/
- GitHub 연동(선택 사항): https://help.zenodo.org/docs/github/

GitHub–Zenodo 연동을 선택하면 새 저장소를 연결한 뒤 release를 보관하는 방법도 있습니다. 자료 유형을 데이터셋으로 명시하고, 자동 등록 전에 저자·이용 조건 등 메타데이터를 완성해야 합니다. 직접 데이터셋 등록 방식이면 GitHub 연동은 필수가 아닙니다.

## Zenodo 화면 입력값

- Resource type: Dataset
- Title: ELEPHANT PerspectiveShift Data: English–Korean model judgments on AITA-NTA-FLIP
- Creator given name: Kyungmin
- Creator family name: Oh
- Affiliation: 연세대학교 심리과학이노베이션 대학원
- Version: 1.0.0
- License: Creative Commons Attribution 4.0 International (CC BY 4.0)
- Description: `metadata/deposit_metadata_draft.json`의 `description` 내용을 복사합니다.
- Upload file: `elephant-perspectiveshift-data-v1.0.0.zip`

ZIP 안에 들어 있는 `.zenodo.json`은 직접 업로드 화면의 입력란을 자동으로 채우지 않습니다. 위 값을 화면에서 입력하세요. DOI를 예약한 뒤 공개 전에 번호를 README에 반영하고 최종 ZIP을 교체할 수 있습니다.

## 공개 완료 기록

데이터셋은 2026-10-05에 공개되었습니다.

- DOI: **10.5281/zenodo.23156290**
- 공개 페이지: https://zenodo.org/records/23156290
- 공개 파일: `elephant-perspectiveshift-data-v1.0.0.zip`

위 등록 절차는 작업 이력 참고용입니다. 현재 레코드에 새 DOI를 예약하거나 동일 데이터셋을 중복 등록하지 않습니다. 공개된 파일을 변경하려면 별도 새 버전이 필요합니다. GitHub README와 인용 정보 수정은 공개된 Zenodo ZIP을 변경하지 않습니다.
