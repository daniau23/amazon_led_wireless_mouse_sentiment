## **Table of results based on traditional ML algo without PCA (using df_clean test data) on  Amazon Reviews Text Data**

Algorithm|text representation|f1-score-macro-avg|AUC-score-avg-macro
|----------- |----------- | ----------- | ----------- |
Logistic Regression|BOW|0.82|0.923
Logistic Regression|TF-IDF|0.79|0.5
KNNClassifier|Glove-twitter-25|0.72|0.89
HistGradientBoostingClassifier|Glove-twitter-50|0.72|0.92
HistGradientBoostingClassifier|Glove-twitter-100|0.75|0.94
HistGradientBoostingClassifier|Glove-twitter-200|0.78|0.95
KNNClassifier|Doc2Vec-PV-DBOW-25|0.75|0.89
KNNClassifier|Doc2Vec-PV-DBOW-50|0.76|0.89
KNNClassifier|Doc2Vec-PV-DBOW-100|0.76|0.89
HistGradientBoostingClassifier|Doc2Vec-PV-DBOW-200|0.67|0.90
Logistic Regression|Doc2Vec-PV-DM-25|0.62|0.85
Logistic Regression|Doc2Vec-PV-DM-50|0.66|0.85
Logistic Regression|Doc2Vec-PV-DM-100|0.66|0.85
Logistic Regression|Doc2Vec-PV-DM-200|0.67|0.85
HistGradientBoostingClassifier|Doc2Vec-Concated(PV-DM + PVDBOW)-25|0.72|0.91
HistGradientBoostingClassifier|Doc2Vec-Concated(PV-DM + PVDBOW)-50|0.72|0.92
Logistic Regression|Doc2Vec-Concated(PV-DM + PVDBOW)-100|0.71|0.89
Logistic Regression|Doc2Vec-Concated(PV-DM + PVDBOW)-200|0.70|0.88

- From the table, it can be seen that as the vector space of word embeddings technique (Glove-twitter) vector space increases, the performance of the algorithm also increases. 
- PV-DBOW seems to be much better than the PV-DM for multiclass classification cases.
- The use of Doc2Vec-Concated(PV-DM + PVDBOW) seems to outperform PV-DM when used alone.
- TF-IDF is the only text representation that experienced random guessing due to AUC score being 0.5.
- Moreover, the stop words exclusion could be improved so the algorithm could be able to identify more negative reviews effectively.

The next step is to make use of deep learning algorithms on the following text represenations namely;
- Glove-twitter-200
- Doc2Vec-PV-DBOW-200
- Doc2Vec-PV-DM-200
- Doc2Vec-Concated(PV-DM + PVDBOW)-200