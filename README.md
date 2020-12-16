# Parkinson's Disease Prediction
This dataset is composed of a range of biomedical voice measurements from 31 people, 23 with Parkinson's disease (PD). Each column in the table is a particular voice measure, and each row corresponds to one of 195 voice recordings from these individuals ("name" column). The main aim of the data is to discriminate healthy people from those with PD, according to the "status" column which is set to 0 for healthy and 1 for PD.

The data is in ASCII CSV format. The rows of the CSV file contain an instance corresponding to one voice recording. There are around six recordings per patient, the name of the patient is identified in the first column.For further information or to pass on comments, please contact Max Little (little '@' robots.ox.ac.uk).

## Dataset Details 
Source: [Center for Machine Learning and Intelligent Systems](http://archive.ics.uci.edu/ml/datasets/Parkinsons/contact.html)
### Dataset citation:
Max A. Little, Patrick E. McSharry, Eric J. Hunter, Lorraine O. Ramig (2008), 'Suitability of dysphonia measurements for telemonitoring of Parkinson's disease', IEEE Transactions on Biomedical Engineering (to appear).

## Model Details:
Here I have used:

* Logistic Regression
* Support Vector Classifier
* Extreme Gradient Boosting

And, used GridSearchCV to hyperparameter tune all of them.

Then used StackingClassifier to Stack all of them into an Ensemble.

Which yielded:

**Accuracy Score 0.9487**

**Classification report:**
|   |precision|recall|f1-score|support|
|:---:|:---:|:---:|:---:|:---:|
|0   |1.00 |     0.71 |     0.83 |        7|
|1   |0.94|      1.00  |    0.97|        32|


## Notebook
Refere the notebook [Parkinson's Disease Prediction.ipynb](https://github.com/aravind-naidu/Parkinson-s-Disease-Prediction/blob/main/Parkinson's%20Disease%20Prediction.ipynb) for the code.
Also, find the same, [here](https://www.kaggle.com/aravindnaidu/94-acc-predicting-parkinson-s-disease-ensemble) on Kaggle and do support mere there with your upvotes and comments.

## Attribute Information:
Matrix column entries (attributes):
* name - ASCII subject name and recording number
* MDVP:Fo(Hz) - Average vocal fundamental frequency
* MDVP:Fhi(Hz) - Maximum vocal fundamental frequency
* MDVP:Flo(Hz) - Minimum vocal fundamental frequency
* MDVP:Jitter(%), MDVP:Jitter(Abs), MDVP:RAP, MDVP:PPQ, Jitter:DDP - Several measures of variation in fundamental frequency
* MDVP:Shimmer,MDVP:Shimmer(dB),Shimmer:APQ3,Shimmer:APQ5,MDVP:APQ,Shimmer:DDA - Several measures of variation in amplitude
* NHR, HNR - Two measures of the ratio of noise to tonal components in the voice
* status - The health status of the subject (one) - Parkinson's, (zero) - healthy
* RPDE, D2 - Two nonlinear dynamical complexity measures
* DFA - Signal fractal scaling exponent
* spread1,spread2,PPE - Three nonlinear measures of fundamental frequency variation
