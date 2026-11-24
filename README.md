# Module 3 생물정보학 보충자료

생물학실험 Module 3의 입력 서열, Phylo.io 원본 계통수와 출처를 모았습니다.
**보고서 본문은 PDF로 별도 제출하며, 이 저장소는 온라인 보충자료입니다.**
보고서 본문, 학번, 조원 사진은 포함하지 않았습니다.

## 바로 보기

- [원본 계통수 PDF — 26쪽](Module3_PhyloIO_originals.pdf)
- [전체 자료 ZIP 다운로드](Module3_bioinformatics_originals.zip)
- 최초 포유류 9종 결과: [COX1 원본 SVG](original_SVG/PhyloIO_Tree_COX1_9mam.svg) · [CYTB 원본 SVG](original_SVG/PhyloIO_Tree_CYTB_9mam.svg)
- [최초 13개 유전자 전체 결과표 CSV](source_metadata/original_13gene_results.csv)
- [추가 11조건 결과표 CSV](source_metadata/additional/additional_tree_audit.csv) · [상세 해석 JSON](source_metadata/additional/additional_tree_audit.json)
- [업로드 파일명·조건·입력 대응표](source_metadata/additional/file_condition_mapping.csv)
- [전체 자료 안내 및 PDF 쪽별 순서](README_KR.txt)

## 자료 구성

| 경로 | 내용 |
|---|---|
| [`original_SVG/`](original_SVG/) | 최초 15개 원본: 기본 COX1, 고인류 포함 COX1, 포유류 9종의 13개 유전자 |
| [`original_SVG/additional/`](original_SVG/additional/) | 종 구성·외군·DNA/아미노산을 비교한 추가 원본 11개 |
| [`input_FASTA/`](input_FASTA/) | 최초 입력 15개와 추가 입력 11개. 정렬 전 DNA CDS 또는 단백질 서열 |
| [`NCBI_original_records/`](NCBI_original_records/) | 서열 출처인 미토콘드리아 GenBank 원문 12개 |
| [`source_metadata/`](source_metadata/) | 원래 서열의 좌표·주석·출처와 추가 입력 검증 기록 |

SVG는 업로드된 원본 바이트를 보존했습니다. 26쪽 PDF는 원본의 뿌리 표시,
종 순서, 가지와 숫자를 유지하며 주변 캔버스와 전체 배치 크기만 조정했습니다.
추가 조건은 시궁쥐 추가 1개, 외군 제외 2개, 대체 외군 DNA 4개,
아르마딜로 외군 아미노산 2개, 주머니쥐 외군 아미노산 2개입니다.

## 서열 accession 찾기

다음은 포유류 비교에 사용한 원본 미토콘드리아 레코드입니다.
각 accession 링크에서 저장된 GenBank 원문을 확인할 수 있습니다.

| 종 | accession.version | 자료에서의 역할 |
|---|---|---|
| 사람 (*Homo sapiens*) | [NC_012920.1](NCBI_original_records/NC_012920.1.gb) | 공통 내군 |
| 침팬지 (*Pan troglodytes*) | [NC_001643.1](NCBI_original_records/NC_001643.1.gb) | 공통 내군 |
| 캐나다비버 (*Castor canadensis*) | [NC_033912.1](NCBI_original_records/NC_033912.1.gb) | 공통 내군 |
| 생쥐 (*Mus musculus*) | [NC_005089.1](NCBI_original_records/NC_005089.1.gb) | 공통 내군 |
| 소 (*Bos taurus*) | [NC_006853.1](NCBI_original_records/NC_006853.1.gb) | 공통 내군 |
| 대왕고래 (*Balaenoptera musculus*) | [NC_001601.1](NCBI_original_records/NC_001601.1.gb) | 공통 내군 |
| 개 (*Canis lupus familiaris*) | [NC_002008.4](NCBI_original_records/NC_002008.4.gb) | 공통 내군 |
| 고양이 (*Felis catus*) | [NC_001700.1](NCBI_original_records/NC_001700.1.gb) | 공통 내군 |
| 버지니아주머니쥐 (*Didelphis virginiana*) | [NC_001610.1](NCBI_original_records/NC_001610.1.gb) | 원래 외군 |
| 시궁쥐 (*Rattus norvegicus*) | [NC_001665.2](NCBI_original_records/NC_001665.2.gb) | 추가 CYTB 비교 |
| 아프리카코끼리 (*Loxodonta africana*) | [NC_000934.1](NCBI_original_records/NC_000934.1.gb) | 대체 외군 |
| 아홉띠아르마딜로 (*Dasypus novemcinctus*) | [NC_001821.1](NCBI_original_records/NC_001821.1.gb) | 대체 외군 |

유전자별 추출 좌표는 [최초 sequence manifest](source_metadata/sequence_manifest.json)와
[추가 출처 폴더](source_metadata/additional/)에 있습니다.

## 분석 기록과 해석 범위

최초 분석의 MAFFT(version 7), NJ, Jukes–Cantor, Conserved sites,
bootstrap 1,000회는 수업과 실험 기록에 근거합니다.
추가 입력의 metadata에는 DNA NJ·JC, 아미노산 NJ·JTT 등의 **제공 안내 조건**도
포함되어 있습니다. 안내 조건은 실제로 확정된 실행 기록과 구분합니다.
SVG 자체에는 정렬 방법·모형·위치 선택·bootstrap 반복 수가 충분히 기록되어
있지 않아, 원본만으로 확인할 수 없는 설정은 결과표에 미확인으로 남겼습니다.

결과표는 원본 SVG의 연결과 표시 숫자를 읽어 정리한 것입니다.
`absent`는 해당 집합이 나타나지 않았다는 뜻이며 지지도 0을 뜻하지 않습니다.
자료를 정리하면서 새 정렬이나 계통수 추론을 실행하지 않았습니다.
조건별 차이만으로 한 가지 원인을 확정하지 않으며, 선택한 결과만 남기지 않고
제공된 조건들을 함께 보관했습니다.

## 파일 동일성 확인

- [`SHA256.csv`](SHA256.csv): 전체 ZIP에 원래 포함된 manifest입니다. 원형을 보존했습니다.
- [`release_manifest.csv`](release_manifest.csv): 이 저장소용 파일 전체를 확인합니다. ZIP 자체와 이 README도 포함하며, manifest 자기 자신은 제외합니다.

해시로 각 파일의 내용이 바뀌었는지 확인할 수 있습니다.
