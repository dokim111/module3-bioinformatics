포유류 9종 비교: 미토콘드리아 유전자별 FASTA 자료
작성일: 2026-11-17

1. 자료의 목적

기존 CYTB 포유류 비교와 같은 9종, 같은 NCBI 미토콘드리아 레코드를 유지하면서
유전자에 따라 계통수 결과가 어떻게 달라지는지 비교하기 위한 자료이다.
각 FASTA에는 한 유전자의 DNA 서열 9개가 들어 있다.
모든 파일은 아직 정렬하지 않은 원본 CDS이며, 유전자별로 따로 MAFFT에 업로드한다.
총 13개 유전자, 117개 서열이다. 계통수와 bootstrap 결과는 아직 생성하지 않았다.

2. 포함된 9종

영장목: Homo_sapiens (사람), Pan_troglodytes (침팬지)
설치목: Castor_canadensis (캐나다비버), Mus_musculus (생쥐)
우제류 계통: Bos_taurus (소), Balaenoptera_musculus (대왕고래)
식육목: Canis_lupus_familiaris (개), Felis_catus (고양이)
외군: Didelphis_virginiana (버지니아주머니쥐, 유대류)

기존 CYTB 파일과 종 이름 및 순서를 동일하게 유지했다.
새로 수록한 CYTB_9species_mammals.fasta는 기존에 제공한 CYTB 파일과 바이트까지 같다.

3. 먼저 비교할 유전자

FASTA/COX1_9species_mammals.fasta : 1542~1551 nt
FASTA/COX2_9species_mammals.fasta : 682~684 nt
FASTA/COX3_9species_mammals.fasta : 781~786 nt
FASTA/ND2_9species_mammals.fasta  : 1038~1044 nt
FASTA/ND4_9species_mammals.fasta  : 1378 nt
FASTA/ND5_9species_mammals.fasta  : 1809~1824 nt
FASTA/ATP6_9species_mammals.fasta : 681 nt

비교 기준:
FASTA/CYTB_9species_mammals.fasta : 1140~1149 nt

이 우선순위는 현재 레코드의 주석, 길이, 처리 편의성을 고려한 것이다.
어떤 유전자가 반드시 기대하는 포유류 계통을 재현한다는 뜻은 아니다.

4. 추가 비교용 유전자

FASTA/ND1_9species_mammals.fasta : 955~957 nt
  침팬지 NC_001643.1의 CDS는 <2725..3681로 5' 경계가 불완전/불확실하게 표시된다.
  시작 부분을 임의로 채우지 않고 원문 범위를 유지했다.

FASTA/ND3_9species_mammals.fasta : 322~349 nt
  캐나다비버 NC_033912.1의 CDS는 <9503..9824이며 시작코돈이 결정되지 않았다는
  주석이 있다. 비버 서열은 322 nt로 다른 종보다 짧다. 원문 그대로 제공한다.

FASTA/ND4L_9species_mammals.fasta : 297 nt
FASTA/ATP8_9species_mammals.fasta : 192~210 nt
  비교적 짧은 유전자이므로 단독 분석에서 충분한 정보를 제공하지 못할 수 있다.

FASTA/ND6_9species_mammals.fasta : 507~528 nt
  9종 모두 음의 가닥에 있으므로 역상보 서열로 변환하여 코딩 방향으로 제공했다.
  사용자가 다시 역상보 변환할 필요는 없다.

5. 실행 방법

(1) https://mafft.cbrc.jp/alignment/server/index.html 에 접속한다.
(2) 비교할 유전자 FASTA 하나를 업로드한다. 첫 비교는 COX1 파일로 시작하면 된다.
(3) DNA 서열 방향은 모두 코딩 방향으로 맞추었으므로 Same as input으로 사용할 수 있다.
(4) 종 이름이 잘리지 않도록 Title length를 50 또는 100으로 설정한다.
(5) 수업에서 정한 동일한 정렬 조건으로 Submit하고, 결과에 9종이 모두 있는지 확인한다.
(6) 정렬 결과 FASTA를 원본과 구별하여 저장한다.
(7) Phylogenetic tree에서 수업 조건을 적용한다.
    Method: NJ - Conserved sites
    Substitution model: Jukes-Cantor
    Bootstrap: On, Number of resampling: 1000
(8) 완료된 tree를 Phylo.io에서 열고 Didelphis_virginiana로 이어지는 가지에서
    Reroot를 선택한다. 주머니쥐가 다른 8종과 먼저 갈라지는지 확인한다.
(9) 유전자 이름, 정렬 길이, 실제 사용 site 수, 설정, 계통수, 지지도를 함께 저장한다.

기존 CYTB 결과와 비교할 항목:
- 사람과 침팬지가 묶이는가?
- 비버와 생쥐가 같은 설치목 그룹을 형성하는가?
- 설치목과 영장목의 관계는 어떠한가?
- 개와 고양이, 소와 대왕고래가 각각 묶이는가?
- 관련 분기의 bootstrap 값은 얼마인가?

서로 다른 유전자를 동일 조건으로 분석하더라도 길이와 진화 특성이 다르다.
한 유전자에서 원하는 모양이 나왔다고 나머지 결과를 버리지 말고 비교 결과를 기록한다.

6. 원서열 처리와 검증

모든 DNA는 NCBI GenBank CDS 좌표에서 추출했다. 길이를 맞추기 위한 자르기,
A/N 추가, 갭 추가는 하지 않았다. ND6에 한해서 원래 코딩 방향을 반영한 역상보
변환을 수행했다. FASTA의 제목은 기존 자료와 같은 종 이름이며 서열 줄에는 A/C/G/T만 있다.

독립적으로 추출한 117개 서열과 전부 일치함을 확인했다.
척추동물 미토콘드리아 유전암호 표 2와 개시·말단 주석을 반영하여 번역했을 때
117개 모두 NCBI의 단백질 번역 주석과 일치했다. 내부 정지코돈과 모호한 염기는 없었다.

39개 CDS에는 mRNA poly(A) 부가로 종결코돈을 완성하는 등의 말단 번역 예외가 있다.
따라서 DNA 길이가 3의 배수가 아니어도 다운로드 오류라고 단정하지 않는다.
코돈 기반 분석 단계에서 말단 정지코돈과 읽는 틀을 별도로 처리해야 한다.

7. 향후 보강 분석에서의 주의

이번 13개 유전자는 모두 미토콘드리아 유전체에 있다. 유전자를 늘리면 비교할
염기 정보량은 늘지만, 13개의 독립적인 종계통 증거가 되는 것은 아니다.
핵유전자 분석은 별도의 보강 단계로 다룬다.

유전자들을 연결한 분석을 하려면 먼저 유전자별로 정렬·검토하고, 동일 종별로
같은 순서로 연결해야 한다. 13개 파일을 117개의 서로 다른 종처럼 한꺼번에
정렬하면 안 된다. 원본 서열을 단순히 이어 붙여 한 번에 정렬하는 방법도 피한다.

일부 CDS는 같은 미토콘드리아 좌표를 공유한다.
- ATP8와 ATP6: 31~46 nt 중첩
- ATP6와 COX3: 9종 모두 1 nt 중첩
- ND4L과 ND4: 9종 모두 7 nt 중첩
- ND5와 ND6: 7종에서 반대 방향으로 4~17 nt 중첩

단독 유전자 파일에서는 원래 범위를 유지했다. 이후 연결 행렬을 만들 때에는
동일한 게놈 위치가 중복 집계되는 문제를 별도로 처리하고 기록해야 한다.

제3 코돈 위치를 제외하는 비교는 읽는 틀이 보존된 코돈 정렬을 먼저 확보한 뒤 수행한다.
일반 DNA 정렬에서 무조건 세 번째 열마다 지우면 갭 때문에 잘못된 위치를 제거할 수 있다.

8. 출처 파일

sequence_manifest.json: 117개 CDS의 종, accession, 좌표, 길이, 방향, 번역 주석,
                       partial 표시, 원본 및 구간 FASTA 링크, 겹치는 게놈 좌표.
source_details.txt: 유전자별 출처를 일반 텍스트로 확인하는 파일.
NCBI_original_records/: 원래 사용한 9개 GenBank 레코드.

NCBI 유전암호 표:
https://www.ncbi.nlm.nih.gov/Taxonomy/Utils/wprintgc.cgi#SG2

FASTA 추출 좌표와 종별 레코드 링크는 위 출처 파일에 모두 기록되어 있다.
