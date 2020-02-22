## IEE-CIS Fraud Detection


**1. Competition Link**
  - https://www.kaggle.com/c/ieee-fraud-detection/overview


**2. Competition Object**
  - For each "TransactionID" in the test set, you must predict a probability for the "isFraud" variable.
  - 평가척도 : AUC(area under the ROC curve)
  

**3. Data & Exploration**
  - https://www.kaggle.com/c/ieee-fraud-detection/data
  - "ProductCD", "card1"등 Transaction 데이터(금융거래관련 데이터)와 "DeviceType", "id_12"등 Identity 데이터(고객정보관련 데이터)로 구성
  - numeric 형태 380개, object 형태 14개 컬럼으로 구성됨(590540 X 394)
  - Target 컬럼은 "isFraud"로 "0"이면 정상, "1"이면 부정. 정상과 부정의 데이터 비율은 정상거래 96.50%, 부정거래 3.50%로 불균형 데이터
  

**4. Reference**
  - https://www.kaggle.com/duykhanh99/lgb-fe-0-9492-lb-newfeature-0-9496-lb

    
    
    
  - https://www.kaggle.com/duykhanh99/lightgbm-feature-engineering-eda-with-r
    - xxx
    
    
    
  - https://www.kaggle.com/kyakovlev/ieee-gb-2-make-amount-useful-again
    - "M1" ~ "M9"의 합, 결측치의 갯수 컬럼 신규생성, "card"별로 "TransactionAmt"의 mean과 std 컬럼 신규생성 등
    - Object형 컬럼 labeling, scipy패키지의 ks_2samp를 이용하여 불필요한 컬럼 제거, 최종 11개 컬럼 선택
    - 1개 LightGBM 알고리즘 사용(주요 파라미터 : num_leaves = 2^8, boosting_type = gbdt, early_stopping_rounds = 100 등)
    - 10-Fold 교차검증    
    - Public Score : 0.946803 
    
    
    
  - https://www.kaggle.com/nroman/lgb-single-model-lb-0-9419
    - 394개 feature중 159개 제거
    - "TranactionAmt"을 int형의 신규 컬럼으로 생성 , "card_1"의 count encoding, 요일/시간 신규 컬럼 생성 등
    - 1개 LightGBM 알고리즘 사용(주요 파라미터 : min_data_in_leaf = 106, boosting_type = gbdt 등)
    - 5-Fold 교차검증, [TimeSerieSplit](https://scikit-learn.org/stable/modules/generated/sklearn.model_selection.TimeSeriesSplit.html)
    - features 중요도는 "card1"과 그 파생변수, "TransactionAmt"가 상대적으로 높음
    - Public Score : 0.941915
    
    
    
  - https://www.kaggle.com/davidcairuz/feature-engineering-lightgbm
    - "DeviceInfo", "id23", "id30" ~ "id34" 관련 신규 컬럼 생성, "TransactionAmt"을 로그화(log), 일부변수 mean, std 값 파생변수생성
    - 394개 feature중 159개 제거
    - 1개 LightGBM 알고리즘 사용(주요 파라미터 : min_data_in_leaf = 106, boosting_type = gbdt 등)
    - 5-Fold 교차검증
    - features 중요도는 "card1"과 그 파생변수, "TransactionAmt"가 상대적으로 높음
    - Public Score : 0.9449 
    
    
    
  - https://www.kaggle.com/kyakovlev/ieee-lgbm-with-groupkfold-cv
    - xxx
    
    
    
  - https://www.kaggle.com/tolgahancepel/lightgbm-single-model-and-feature-engineering
    - xxx
    
    
    
  - https://www.kaggle.com/rafay12/is-it-really-fraud
    - xxx
    
    
    
  - https://www.kaggle.com/ysjf13/cis-fraud-detection-visualize-feature-engineering
    - xxx
    
    
    
  - https://www.kaggle.com/whitebird/a-method-to-valid-offline-lb-9506
    - xxx
    
    
    
  - https://www.kaggle.com/kyakovlev/ieee-simple-lgbm
    - xxx
    
    
    
**5. Ensemble**
  - XXX

**6. Result**
  - XXX
