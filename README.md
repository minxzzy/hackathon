#### 팀명 : Team ValueUP
-  이유 : 한국의 밸류업 프로그램으로 기업의 가치가 올라가는 것처럼 현재 과정을 수행하는 우리의 가치도 한 단계 성장하자는 의미.

1. 팀프로젝트명/이유 : 한국의 밸류업 프로그램에 대한 기업 수익률 검증

   - 이유 : 우리나라가 밸류업프로젝트를 한 이유는 주주환원율 낮아서 기업이 문제가 있다!

     정부의 밸류업 프로젝트는 주주환원율 높이는 기업들 우대해주고 세제혜택 주겠다 그게 밸류업을 시키는 사실이 될까를 보려면 

     과거의 그런 기업들의 성과가 연평균수익률이 차이가 있겠지만 유의한가

   - 타켓이 누구인지

   - 솔류션을 제공해주기 위한 타켓

   - 타겟: 정부의 주장이 사실인지 검증 후 투자자입장에서 투자 결정

   

2. 이 주제에 대한 문제점 제시/ 해결방법

   - 어떤 기업의 성과가(초과수익률이 )높을까

   - PBR 1 미만인 기업이 저평가 되있다

   - 주주환원율: 회사가 이익이 나면 배당율/ 유보율

   - 배당 말고 배당할 이익으로 자사주 매입(->주주환원율)

   - 주주환원율: 배당과 자사주 매입액의 합을 순이익으로 나누 비율

   - 코스피나 코스닥 나눠보기 

   - PBR/ 주주환원율 4개의 그룹이 나온다.(분위수로 나눠서)

   - H      H

   - H      L

   - L       H : 이 기업의 성과가 주주의 수익률이 다른 집단보다 높은가를 검증하는 것

   - L       L

     

3. 해결 방법

4. 목표 방향, 데이터 설명(확보 가능성, 구성)

5. 타임테이블(4월1일까지)10번+주말2






#### 본론
### 데이터 셋
- 데이터 대상 기업


### 데이터 수집 기간
- 경기 순환 국면 제 8순환기(2001.07 저점에서 저점부터) 현재까지
- 어디서? 네이버 증권, 야후 등 에코스 프레드 다트 카인드 ts2000 신뢰도 때문eda 데이터 탐색 및 전처리

### EDA(데이터 탐색 및 전처리)
- describe(기초통계량) 
- boxplot(4분위수-이상치 값 판단,이상치 제거 양쪽 0.1 제거?)
- 결측치 처리 어떻게? 정규성이라면 mean
- 상관분석, 회귀분석 : 독립성, 선형성, 정규성, 등분산성(levene테스트) -> 잔차검증
- 선형관계 검증
- 독립성 - DW(Durbin-Watson)test 도 2에 가까우면 독립적,ACF
- 정규성 - qqplot, shapriowilk
- 등분산성(levene테스트)
- 스케일링
- 처리 후 데이터 분포 보여주기

### 피쳐(피쳐셀렉션)
- pbr
- 주주환원율 ts2000
- 배당성향
- 자사주매입
- 다중공선성
- 펌사이즈

### 모델링(방법)
- 파마프렌치 3펙터 모델
- 다중회귀분석
- 파마 맥배스 검증 참고 (다중회귀 다중공선성)

### 인사이트/ 연구정과정에서의 한계(데이터셋, 시간 등)
- 어떨때 성장주가 많이 오를까? 금리가 높은 수준 낲은 수준 회귀계수가 어떻게 변하는지

- 경기가 좋았을 때 20년치 경기 확장기에서의 파마 3펙터 계수가 음수인지 양수인지

- 금리수준으로 나누나 3.5 이상 고금리 2.5미만  저금리 그 사이 중립지대
  - 대립가설 금리구간에 따라 기업규모에 따른 수익률의 차이가 있을 것이다
  - 귀무가설 차이가 없다. 어떻게 차이가 있나 소형주와 대형주

- 일별 종가수익률 무엇으로 할 것인지 단순수익률 또는 로그 수익률

- 스켈링 하고 표준화하기
