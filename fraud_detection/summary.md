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
  - Target 컬럼은 "isFraud"로 0이면 정상, 1이면 부정. 정상과 부정의 데이터 비율은 정상거래 96.50%, 부정거래 3.50%로 불균형 데이터
  

**4. Reference**
  - https://www.kaggle.com/duykhanh99/lgb-fe-0-9492-lb-newfeature-0-9496-lb
    - 394개 feature중 159개 제거
    - 
    
    
    
  - https://www.kaggle.com/duykhanh99/lightgbm-feature-engineering-eda-with-r
    - xxx
    
    
    
  - https://www.kaggle.com/kyakovlev/ieee-gb-2-make-amount-useful-again
    - xxx
    
    
    
  - https://www.kaggle.com/nroman/lgb-single-model-lb-0-9419
    - 394개 feature중 159개 제거
    
    
    
  - https://www.kaggle.com/davidcairuz/feature-engineering-lightgbm
    - xxx
    
    
    
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
