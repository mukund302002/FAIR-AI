# FAIR-AI
A kaggle contest organized by te cse dept of IIT BHU.

# Overview
In the Enigma machine-learning competition, participants are tasked with crafting a model that not only excels in accuracy but also embodies the principles of fairness. Accuracy, the cornerstone of any effective model, entails the ability to make precise predictions or classifications with minimal error. However, in pursuit of this precision, fairness must not be sacrificed. Fairness ensures that the model's decisions do not perpetuate biases or discriminate against particular groups, thus upholding ethical standards. Achieving both accuracy and fairness requires a delicate balance, necessitating thoughtful feature engineering, unbiased dataset selection, and rigorous evaluation metrics. Participants must demonstrate their ability to navigate this intricate landscape, showcasing their prowess in constructing models that are not only technically proficient but also ethically sound, contributing to the advancement of responsible AI.
Ranking of solutions will be according to their fairness with respect to the provided genders. In other words, we want you to design a competitive solution that is not biased towards one gender in particular. To be specific, we will use Demographic Parity Ratio as our fairness metric to measure the fairness of your machine learning model.

# About Dataset
The dataset has 16 feature including the prediction column.
The columns where -:
ID
LIMIT_BAL
SEX
EDUCATION
MARITAL_STATUS
AGE
INSTALLMENT_1
INSTALLMENT_2
INSTALLMENT_3
INSTALLMENT_AMT_1
INSTALLMENT_AMT_2
INSTALLMENT_AMT_3
INSTALLMENT_PAID_1
INSTALLMENT_PAID_2
INSTALLMENT_PAID_3
DEFAULT.PAYMENT.NEXT.MONTH

where the prediction column is the DEFAULT.PAYMENT.NEXT.MONTH with binary values.
The dataset consists of 30,000 datapoints. The training data comprises of 21,000 data samples and rest is test set.

# Approach
- Label encoded the non-categorical columns.
- Managing the imbalancing by RANDOMOVERSAMPLER, imporoving the DPR ratio.
- Implemented a stacking ensemble technique with RandomForest, XGBoost and AdaBoost and thye base classifiers and applying KNN as the last layer model for final classification output.

# Results
- Our overall public score was 0.522 and private score was .511.
- Our team got 3rd position in the contest.
