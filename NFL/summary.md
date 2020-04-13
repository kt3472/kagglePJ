## NFL Big Data Bowl

**1. Competition Link**
  - https://www.kaggle.com/c/nfl-big-data-bowl-2020


**2. Competition Object**
  - For each playerID, we must predict a cumulative probability distribution for the yardage gained or lost.
  - 평가척도 : CRPS(Continuous Ranked Probability Score, 예측값의 누적분포함수와 실제값의 누적분포함수 간의 차이)


**3. Data & Exploration**
  - https://www.kaggle.com/c/nfl-big-data-bowl-2020/data
  - 2017년 부터 2018년까지 총 512회 미식축구경기 플레이어들의 정보인 field에서의 위치(location), 속도(speed), 가속도(velocity) 등과, 날씨정보, 경기장의 상태정보 등 49개 컬럼으로 구성
  - Numeric형 25개, object형 24개로 구성  


**4. Preprocessing & Feature Eng.**
- rushing player 기준으로 데이터 병합 및 정리
- 공/수 여부, 방향데이타, 각도 등를 반영한 location관련 신규 데이터 생성
- 선수들의 나이,신장, 경기시간 날씨 등의 다향한 형식으로 표현된 value를 동일한 형태로 전처리  


**5. Model tuning**
- 랜덤포레스트 1개 + 인공신경망 1개
- 각 모델별 5 fold 교차검증


**6. Ensemble**
- Test 결과값을 기준으로 모델별 최적 비중을 계산 
- 랜덤포레스트 0.25, 인공신경망 0.75 가중평균


**7. Results**
- CRPS = 0.013287 (public/pravate 리더보드 동일)


**8. Reference**
  - https://www.kaggle.com/gogo827jz/blending-nn-and-lgbm-rf
  - https://www.kaggle.com/ben519/understanding-x-y-dir-and-orientation
  - https://blog.naver.com/madden789
