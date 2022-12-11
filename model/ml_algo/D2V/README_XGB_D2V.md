## **XGB USAGE**
Algorithm|text representation|f1-score-macro-avg|AUC-score-avg-macro
|----------- |----------- | ----------- | ----------- |
Extreme Gradient Boosting|Doc2Vec-PV-DBOW-25|0.73|0.91
Extreme Gradient Boosting|Doc2Vec-PV-DBOW-200|0.76|0.92
Extreme Gradient Boosting|Doc2Vec-PV-DM-25|0.74|0.91
Extreme Gradient Boosting|Doc2Vec-PV-DM-200|0.73|0.91
Extreme Gradient Boosting|Doc2Vec-Concated(PV-DM + PVDBOW)-25|0.73|0.91
Extreme Gradient Boosting|Doc2Vec-Concated(PV-DM + PVDBOW)-200|0.76|0.92

Making use of the following for model deployment on streamlit;
- Extreme Gradient Boosting Doc2Vec(PV-DM)-25
- Extreme Gradient Boosting Doc2Vec(PVDBOW)-25
- Extreme Gradient Boosting Doc2Vec(PV-DM)-200 
- Extreme Gradient Boosting Doc2Vec-Concated(PV-DM + PVDBOW)-200