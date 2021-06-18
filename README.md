# Ensemble-MFP
Predicting Drug-Target Interactions based on the Ensemble Models of Multiple Feature Pairs



Backgroud: The prediction of drug-target interactions (DTIs) is of great significance in drug development. It is time-consuming and expensive in traditional experimental methods. Machine learning can reduce the cost of prediction and is limited by the characteristics of imbalanced datasets and problems of essential feature selection. 

Methods: The prediction method based on Ensemble model of Multiple Feature Pairs (Ensemble-MFP) is introduced. Firstly, three negative sets are generated according to the Euclidean distance of three feature pairs. Then, the negative samples of validation set / test set are randomly selected from the union set of the three negative sets in validation set / test set. At the same time, the ensemble model with weight is optimized and applied to the test set. 

Results: The area under the receiver operating characteristic curve (area under ROC, AUC) in 3 out of 4 sub-datasets in gold standard datasets were more than 94.0\% in the prediction of new drugs. The effectiveness of proposed method are also shown with the comparison of state-of-the-art methods and demonstration of predicted drug-target pairs.

Conclusion: The Ensemble-MFP can weight the existing feature pairs and has good prediction effect for general prediction on new drugs.
