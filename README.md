# Ensemble-MFP
Predicting Drug-Target Interactions based on the Ensemble Models of Multiple Feature Pairs

This code is used for the algorithm named "Ensemble Models of Multiple Feature Pairs (Ensemble-MFP)" for drug-target interaction predictions, and cannot be used for commercial purposes without the permission of the authors.


The dataset can be download from http://web.kuicr.kyoto-u.ac.jp/supp/yoshi/drugtarget/, the part of "Adjacency matrix of the gold standard drug-target interaction data" is used in the algorithm.

In the code of "feature_check", we need to use the drugs/targets descriptors. These data can be obtained according to PaDEL-Descriptor (http://padel.nus.edu.sg) and PROFEAT (http://bidd2.nus.edu.sg/), and the environment parameter "filepath_drug/filepath_target" should be changed according to the storage location of the data. Libsvm can be downloaded at https://www.csie.ntu.edu.tw/~cjlin/libsvm/.

Backgroud: The prediction of drug-target interactions (DTIs) is of great significance in drug development. It is time-consuming and expensive in traditional experimental methods. Machine learning can reduce the cost of prediction and is limited by the characteristics of imbalanced datasets and problems of essential feature selection. 

Methods: The prediction method based on Ensemble model of Multiple Feature Pairs (Ensemble-MFP) is introduced. Firstly, three negative sets are generated according to the Euclidean distance of three feature pairs. Then, the negative samples of validation set / test set are randomly selected from the union set of the three negative sets in validation set / test set. At the same time, the ensemble model with weight is optimized and applied to the test set. 

Results: The area under the receiver operating characteristic curve (area under ROC, AUC) in 3 out of 4 sub-datasets in gold standard datasets were more than 94.0\% in the prediction of new drugs. The effectiveness of proposed method are also shown with the comparison of state-of-the-art methods and demonstration of predicted drug-target pairs.

Conclusion: The Ensemble-MFP can weight the existing feature pairs and has good prediction effect for general prediction on new drugs.


Explanations of some codes,

main.m		-->		The main code

Parameter_adjust.m		-->	  The code is used to adjust parameters in SVM (c and gamma)

AUC_cal.m			  -->	        Calculate the AUC

feature_check.m			 -->	   Load and define the feature descriptor files

Fold_div_vali.m			-->	    Divide the dataset based on the ratio 3:1:1

ran_select.m		-->		      Randomly select samples
