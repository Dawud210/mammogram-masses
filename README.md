## Predicting whether a mammogram mass is benign or malignant

Mammography is an effective method for breast cancer screening and to predict wheather the mass screened ("mammogram mass") is benign or malignant I
Will be using the "mammographic masses" public dataset from the UCI repository (source: https://archive.ics.uci.edu/ml/datasets/Mammographic+Mass) that 

contains 961 instances of masses detected in mammograms, and contains the following attributes:


   1. BI-RADS assessment: 1 to 5 (ordinal)  
   2. Age: patient's age in years (integer)
   3. Shape: mass shape: round=1 oval=2 lobular=3 irregular=4 (nominal)
   4. Margin: mass margin: circumscribed=1 microlobulated=2 obscured=3 ill-defined=4 spiculated=5 (nominal)
   5. Density: mass density high=1 iso=2 low=3 fat-containing=4 (ordinal)
   6. Severity: benign=0 or malignant=1 (binominal)
   
BI-RADS is measure of how confident is the severity classification of the mammographic mass is, it is not a predictive attribute and so i have discarded it. The age, shape, margin, and density attributes are the features that we will build our model with, and "severity" is the classification we will attempt to predict based on those attributes.

A lot of unnecessary anguish and surgery arises from false positives arising from mammogram results. If I can build a better way to interpret them through supervised machine learning, it could improve a lot of lives.

I have applied six different supervised machine learning techniques to this data set, and see which one yields the highest accuracy as measured with K-Fold cross validation (K=10) where the data is divided into ten difrrent folds that will be tested iteratively. 

* Decision tree
* Random forest
* KNN
* Naive Bayes
* SVM


The data has been cleaned so that many rows contain missing data and identifiable outliers aswell as any erroneous data will be removed.
I have used tuned hyperparameters for many techniques to achieve over 80 percent accuracy. To see my work click on Predicting whether a mammogram mass is benign or malignant jupyter notebook it might say something is wrong dont wprry just click on reload. 
