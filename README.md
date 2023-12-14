Prediction Sleeping Efficiency
==============================
1. 프로젝트 동기 및 주제 소개

현대에 와서 수면 효율이 낮거나, 수면 장애를 가지고 있는 사람들이 많아지고 있다. 어떤 날은 오래 자도 피로가 풀리지 않을 때가 있기도 한다.
여기서 '수면 효율(Sleep Efficiencty)'이란, 얼마나 효율적으로 잠을 자는지를 나타내는 지표를 뜻한다.
수면 효율은 실제로 잠을 잔 시간 / 침대에 누워있는 시간으로 파악한다.
이처럼 충분한 수면 시간도 중요하지만, 깊은 잠과 얕은 잠의 비율도 중요할 것이다. 또한, 수면의 질을 결정하는 데에 다른 요소들도 있을 것이다.
따라서, 나는 어떤 요인이 수면효율을 결정하는 데 큰 영향을 미치며, 여러 요인들을 바탕으로 수면 효율을 예측하는 모델을 만들어보기로 결심했다.


2. 데이터 선정

Data set은 Kaggle에서 살험 대상자 그룹의 수면 패턴에 대한 정보를 포함하는 'Sleep Efficiency Dataset'을 선택했다.

Data의 각 features을 소개하자면,
- ID: 실험 대상자 번호
- Age: 나이
- Gender: 성별
- Bedtime: 침대에 누운 시간
- Wakeup time: 일어난 시간 
- Sleep duration: 수면 시간
- Sleep efficiency: 수면 효율
- Rem sleep percentage: 전체 수면에서 REM 수면 비율
- Deep sleep percentage: 전체 수면에서 깊은 수면 비율
- Light sleep percentage: 전체 수면에서 얕은 수면 비율
- Awakenings: 자면서 일어난 횟수
- Caffeine consumption: 수면 전 24시간 이내 카페인 섭취량
- Alcohol consumption: 수면 전 24시간 이내 알코올 섭취량
- Smoking status: 흡연 여부
- Exercise frequency: 운동 빈도
이다.


3. 데이터 전처리

수면 효율은 침대에 누운 시간과 실제로 잠을 잔 시간으로 결정되기 때문에, target인 feature에서
