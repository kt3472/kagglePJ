## M5 Forecasting - Accuracy

**1. Competition Link**
  - https://www.kaggle.com/c/m5-forecasting-accuracy/overview


**2. Competition Object**
  - Forecasting daily sales for the next 28 days with hierarchical sales data from Walmart 
  - 평가척도 : RMSSE(Weighted Root Mean Squared Scaled Error)


**3. Data & Exploration**
  - https://www.kaggle.com/c/m5-forecasting-accuracy/data
  - 
  - 


**4. preprocessing & Feature Eng.**
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
- RMSSE = 0.013287 (public/pravate 리더보드 동일)


**8. Reference**
  - https://www.kaggle.com/rodrigolima82/time-series-analysis-es-sarimax-xgb-lgbm
