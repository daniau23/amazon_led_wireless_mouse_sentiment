## **Table of results based on traditional ML algo without PCA (using df_clean test data) on  Amazon Reviews Text Data**

Algorithm|text representation|f1-score-macro-avg|AUC-score-avg-macro
|----------- |----------- | ----------- | ----------- |
Logistic Regression|BOW|0.82|0.923
Logistic Regression|TF-IDF|0.79|0.5
KNNClassifier|Glove-twitter-25|0.72|0.89
HistGradientBoostingClassifier|Glove-twitter-50|0.72|0.92
HistGradientBoostingClassifier|Glove-twitter-100|0.75|0.94
HistGradientBoostingClassifier|Glove-twitter-200|0.78|0.95
Simple Neural Network|Glove-twitter-200|0.74|0.90
Convolutional Neural Network|Glove-twitter-200|0.82|0.96
LSTM|Glove-twitter-200|0.24|0.51
Bidirectional-LSTM|Glove-twitter-200|0.82|0.96
GRU|Glove-twitter-200|0.24|0.50
Bidirectional-GRU|Glove-twitter-200|0.82|0.96
KNNClassifier|Doc2Vec-PV-DBOW-25|0.75|0.89
KNNClassifier|Doc2Vec-PV-DBOW-50|0.76|0.89
KNNClassifier|Doc2Vec-PV-DBOW-100|0.76|0.89
HistGradientBoostingClassifier|Doc2Vec-PV-DBOW-200|0.67|0.90
Simple Neural Network|Doc2Vec-PV-DBOW-200|0.25|0.80
Convolutional Neural Network|Doc2Vec-PV-DBOW-200|0.53|0.87
LSTM|Doc2Vec-PV-DBOW-200|0.24|0.50
Bidirectional-LSTM|Doc2Vec-PV-DBOW-200|0.24|0.83
GRU|Doc2Vec-PV-DBOW-200|0.24|0.48
Bidirectional-GRU|Doc2Vec-PV-DBOW-200|0.51|0.81
Logistic Regression|Doc2Vec-PV-DM-25|0.62|0.85
Logistic Regression|Doc2Vec-PV-DM-50|0.66|0.85
Logistic Regression|Doc2Vec-PV-DM-100|0.66|0.85
Logistic Regression|Doc2Vec-PV-DM-200|0.67|0.85
Simple Neural Network|Doc2Vec-PV-DM-200|0.73|0.87
Convolutional Neural Network|Doc2Vec-PV-DM-200|0.79|0.94
LSTM|Doc2Vec-PV-DM-200|0.24|0.51
Bidirectional-LSTM|Doc2Vec-PV-DM-200|0.83|0.95
GRU|Doc2Vec-PV-DM-200|0.24|0.50
Bidirectional-GRU|Doc2Vec-PV-DM-200|0.83|0.94
HistGradientBoostingClassifier|Doc2Vec-Concated(PV-DM + PVDBOW)-25|0.72|0.91
HistGradientBoostingClassifier|Doc2Vec-Concated(PV-DM + PVDBOW)-50|0.72|0.92
Logistic Regression|Doc2Vec-Concated(PV-DM + PVDBOW)-100|0.71|0.89
Logistic Regression|Doc2Vec-Concated(PV-DM + PVDBOW)-200|0.70|0.88
Simple Neural Network|Doc2Vec-Concated(PV-DM + PVDBOW)-200|0.73|0.87
Convolutional Neural Network|Doc2Vec-Concated(PV-DM + PVDBOW)-200|0.81|0.95
LSTM|Doc2Vec-Concated(PV-DM + PVDBOW)-200|0.24|0.5
Bidirectional-LSTM|Doc2Vec-Concated(PV-DM + PVDBOW)-200|0.82|0.95
GRU|Doc2Vec-Concated(PV-DM + PVDBOW)-200|0.82|0.95
Bidirectional-GRU|Doc2Vec-Concated(PV-DM + PVDBOW)-200|0.84|0.95


**While using ML ALGO**
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

*NB:* Refer to vectorsize_200_dm_mean for PV-DM-200 for ml_algo

**While using Deep Learning Models**
- From the table above, it can be seen that LSTM and GRU performs terribly with Glove-twitter-200 compared to that of the use of Simple Neural Network and both Bidirectional approaches of LSTM and GRU. **Recommended model to use Convolutional Neural Network (less training time)**
- It seems that the use of PV-DBOW with a vector size of 200 with neural network models does not improve its performance metrics. It seems the use of PV-DBOW will perform better with the use of a smaller vector space as shown in the table above. **Recommended model to use KNNClassifier (less training time)** 
- It can be seen that using PV-DM-200 with neural network models does improve its overall performance except with the use of LSTM and GRU (unidirectional models). **Recommended models to use Bidirectional-LSTM or Convolutional Neural Network**
- Using Doc2Vec-Concated(PV-DM + PVDBOW)-200 with neural network models does improve the performance metrics except with the use of LSTM. **Recommended models to use Bidirectional-GRU or Convolutional Neural Network (less training time)**