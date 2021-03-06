# 기술통계

> 대표되는 몇 개의 숫자로 데이터 전체를 요약하여 양적으로 축소하거나 정리된 표나 그래프를 통하여 데이터의 특징을 파악하는 방법

1. 변수

   - 질적변수
      - 명목형 변수 : 변수가 크기나 순서에 대한 의미가 없고 이름만 의미를 부여할  수 있는 경우
      - 순서형 변수 : 변수가 어떤 기준에 따라 순서에 의미를 부여할 수 있는 경우

   - 양적변수
      - 이산형 변수 : 변수가 취할 수 있는 값을 하나하나 셀 수 있는 경우 
      - 연속형 변수 : 변수가 구간 안의 모든 값을 가질 수 있는 경우 




2. 특성기준에 따른 측정값 분류

   1. 대표치 : 관찰된 자료가 어느 위치에 집중되어있는가
      - 평균(mean)
         - 중심위치로서 의미를 갖는다.
         - 이상값에 의해 변동이 심하게 올 수 있다

      - 중앙값(median)
         - 데이터를 오름차순 정렬 후 중앙에 위치한 값
         - 특이점이 있는 경우에 영향을 덜 받는다
         - 하지만 평균이 정확성이 높다

      - 최빈값(moda)
         - 관측빈도가 가장 많은 값
         - 질적변수의 대표값을 나타내는 방법으로 사용
         - 유일하지 않을 수 있다



   2. 산포도 : 자료들이 어느정도 흩어져있는가
      - 범위(range)
         - 조사된 데이터의 최대값에서 최소값을 뺀 것
         - 특이점이 있는 경우 영향을 크게 받는다

      - 사분위수 범위(IQR)
         - 전체 데이터 중 가운데 50% 데이터의 산포도를 측정
         - 범위와 유사하지만 양극단 값에 영향을 받지 않는다

      - 분산(variance)
         - 데이터가 평균으로부터 흩어진 정도
         - 편차의 제곱의 합으로 계산
         - 모분산은 모집단의 수(N)로 나누고 표본분산은 표본의 수 에서 1을 뺀 자유도(n - 1)로 나누어 계산

      - 표준편차(standard deviation)
         - 분산의 양의 제곱근 값
         - 평균에서 흩어진 정도를 나타냄

      - 변이계수(CV : CV:coefficient of variation) == 변동계수
         - 측정단위가 다른 자료의 흩어진 정도를 상대적으로 비교할 때 사용
         - 표준편차를 표본평균으로 나눈 값

      - 표준화점수(standardized score)
         - 데이터가 평균으로부터 표준편차의 몇배만큼 떨어져 있는지 나타냄

      - 공분산(covariance)
         - 2개 이상의 연속성 변수의 관계설을 확인

      - 상관계수(correlation of coefficient)
         - 두 변수 사이의 연관성을 수치로 객관화
         - -1 <= 1 사이의 값을 가짐
         - 1에 가까울 수록 양의 상관관계, -1에 가까울 수록 음의 상관관계, 0이면 무상관