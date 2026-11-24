생물학실험 Module 3: 입력 자료와 Phylo.io 원본 계통수

1. 자료 구성과 보존

최초 자료와 추가 실험 결과를 한 묶음으로 정리했다. 최초 42개 source 파일의
내용은 바이트 단위로 그대로 유지했고, 추가 SVG 11개와 입력 FASTA 11개,
새 종의 GenBank 3개 및 출처·검증 기록을 덧붙였다.
보고서용으로 다시 그린 계통수는 이 원본 SVG 모음에 포함하지 않았다.

Module3_PhyloIO_originals.pdf: 원본 SVG 26개를 한 쪽에 하나씩 배치한 26쪽 PDF.
원본의 뿌리 표시·종 순서·가지·숫자·기하 구조를 바꾸지 않았다. 글자가
잘리지 않도록 주변 캔버스를 늘리고 전체 그림을 같은 비율로 확대·축소했다.
각 그림의 표시 방향은 원본과 같아 본문에서 외군을 통일한 그림과 다를 수 있다.

original_SVG/: 최초 원본 15개
  기본 실습 COX1 6서열, 고인류 포함 COX1 8서열, 포유류 9종의 13개 유전자.
original_SVG/additional/: 추가 원본 11개
  시궁쥐 추가 CYTB 1개, 외군 제외 DNA 2개, 대체 외군 DNA 4개,
  아르마딜로 외군 아미노산 2개, 원래 주머니쥐 외군 아미노산 2개.

input_FASTA/: 총 26개
  최초 15개 입력을 유지하고 additional/에 추가 11개 조건의 입력을 넣었다.
  DNA 파일은 정렬 전 CDS이고, 아미노산 파일은 공식 GenBank translation
  주석을 바탕으로 준비한 정렬 전 단백질 서열이다.
  중복 CYTB 입력은 최초 묶음과 동일하게 한 번만 보관했다.

NCBI_original_records/: 총 12개
  최초 포유류 9종의 GenBank 9개와 시궁쥐(NC_001665.2),
  아프리카코끼리(NC_000934.1), 아홉띠아르마딜로(NC_001821.1) 원문 3개.

source_metadata/: 최초 출처 자료를 그대로 유지했다.
source_metadata/additional/: 추가 입력 출처·검증·업로드 파일명 대응과
  additional_tree_audit.csv/json을 수록했다. 이 audit는 원본 SVG의 연결과
  표시 숫자를 읽어 정리한 표이며 새 계통수를 추론한 결과가 아니다.

2. PDF 쪽별 순서

1: COX1 기본 영장류 6서열
2: COX1 고인류 포함 8서열
3-15: 최초 포유류 9종의 COX1, COX2, COX3, CYTB, ND1, ND2, ND3,
      ND4, ND4L, ND5, ND6, ATP6, ATP8 순서
16: CYTB DNA, 시궁쥐 추가 10종(주머니쥐 포함)
17: COX1 DNA, 주머니쥐 제외 8종
18: CYTB DNA, 주머니쥐 제외 8종
19: COX1 DNA, 아르마딜로 외군 9종
20: CYTB DNA, 아르마딜로 외군 9종
21: COX1 DNA, 코끼리 외군 9종
22: CYTB DNA, 코끼리 외군 9종
23: COX1 아미노산, 아르마딜로 외군 9종
24: CYTB 아미노산, 아르마딜로 외군 9종
25: COX1 아미노산, 원래 주머니쥐 외군 9종
26: CYTB 아미노산, 원래 주머니쥐 외군 9종

추가 SVG의 정리된 파일명과 실제 업로드 파일명은
source_metadata/additional/file_condition_mapping.csv에 대응시켰다.
이름을 정리했더라도 SVG 파일 내용은 업로드 원본과 바이트 단위로 같다.

3. 실행 기록과 자료의 범위

최초 15개 결과에 관한 사용자 기록은 다음과 같다.
- 실습일: 2026년 11월 17일
- MAFFT 온라인 서버(version 7) 정렬
- Neighbor-Joining, Conserved sites, Jukes-Cantor, bootstrap 1,000회
- Phylo.io 표시 및 SVG 출력
이는 사용자 기록을 정리한 것이며 서버에서 발급한 실행 로그가 아니다.

추가 입력의 provenance에는 준비 당시 계획과 검증 내용이 들어 있다.
DNA에 NJ·JC, 아미노산에 NJ·JTT 등의 계획이 적혀 있어도 이를 SVG만으로
검증된 실행 설정으로 취급하지 않는다. 실제 정렬 방법·거리 모형·위치
선택·bootstrap 반복 횟수는 SVG에 충분히 기록되어 있지 않으므로 추가
파일 대응표와 audit에는 미확인으로 남겼다. 보고서에서 실제 수행 조건을
적을 때는 사용자의 실험 기록을 근거로 삼는다.

입력 준비 provenance의 '아직 정렬·추론을 하지 않았다'는 문장은 준비
시점의 기록이며, 이후 사용자가 제공한 결과는 original_SVG/additional/에 있다.
이번 묶음 정리 작업은 파일 보존·SVG 해석·PDF 배치만 수행했다.
정렬 완료 FASTA, Newick, 서버 실행 로그를 임의로 만들어 추가하지 않았다.
새 ML·UPGMA·유전자 연결 분석을 실행한 자료도 아니다.

외군 없는 결과는 무근 분할로 비교한다. 단순히 화면에 보이는 뿌리를
조상 분기 순서의 증거로 사용하지 않는다. audit의 absent 또는 빈칸은
그 집합이 없다는 뜻이며 지지도 0을 뜻하지 않는다.

4. 파일 동일성 확인

SHA256.csv에는 자기 자신을 제외한 모든 파일의 상대 경로·크기·SHA-256이
들어 있다. 추가 자료만의 목록은 source_metadata/additional/
SHA256_extension.csv에 있다. 값은 현재 파일 내용의 동일성 확인용이며
실제 수행자나 분석 실행 일시를 증명하지 않는다.

원본 PDF의 26개 그림은 SVG subtree와 종명·숫자의 일치를 확인했다.
PDF에는 시스템 Noto 계열 폰트를 사용했고 개인 Macmetrics·proof 폰트를
포함하지 않았다. 원본 SVG 파일 자체의 글꼴 속성은 수정하지 않았다.
