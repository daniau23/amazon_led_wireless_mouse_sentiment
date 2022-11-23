## **Table of results based on traditional ML algo without PCA (using df_clean test data)**

Algorithm|text representation|f1-score-macro-avg|AUC-score-avg-macro
|----------- |----------- | ----------- | ----------- |
Logistic Regression|BOW|0.82|0.923
Logistic Regression|TF-IDF|0.79|0.5
KNNClassifier|Glove-twitter-25|0.72|0.89
HistGradientBoostingClassifier|Glove-twitter-50|0.72|0.92
HistGradientBoostingClassifier|Glove-twitter-100|0.75|0.94
HistGradientBoostingClassifier|Glove-twitter-200|0.78|0.95

From the table, it can be seen that as the vector space of word embeddings technique (Glove-twitter) vector space increases, the performance of the algorithm also increases. Moreover, the stop words exclusion could be improved so the algorithm could be able to identify more negative reviews effectively.

*NB: DOC2VEC is yet to be used to see it's performance.*