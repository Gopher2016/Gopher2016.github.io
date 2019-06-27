---
layout: post
title: Classifying Benign and Malignant Breast Tissue
---

The Centers for Disease Control and Prevention has reported breast cancer to be one of the
leading forms of cancer affecting women in the United States, second only skin cancer, with approximately 240,000 new cases of breast cancer diagnosed every year. I tested several classification models with the intention of identifying specific features of breast cancer tissue that can help predict whether tumor tissue is benign or malignant.

In order to accomplish this task a number of factors were considered in this analysis. Data was obtained from the online machine learning community Kaggle in which various features were computed from digitized images of fine needle aspirate (FNA) of breast mass tissue. The features describe characteristics of the cell nuclei present in the image with metrics relating to cellular radius, texture, perimeter, area, smoothness, compactness, concavity, and symmetry. Each observation within the data set was labeled as being either benign or malignant tissue.

K-nearest neighbors (KNN), logistic regression, naive Bayes, decision tree, and random forest classification algorithms were tested and evaluated for their ability to predict whether a given tissue sample was benign or malignant. All models tested were optimized for recall such that the greatest proportion of tissue samples that were truly malignant could be detected. The logistic regression model was found to have the greatest recall among all other models tested with a recall score of 92% which is shown in the confusion matrix below in which 58 of the 63 total malignant tissue samples within the hold out set were actually predicted to be malignant.

![Distribution](https://github.com/Gopher2016/Gopher2016.github.io/blob/master/images/Logistic_Regression_Confusion_Matrix.png?raw=true)

Aside from being the best performing model that was tested, another advantage of the logistic regression classifier used in this analysis was model interpretability and the ability to evaluate feature importance. Among the features that were of greatest importance in classifying between benign and malignant tissue were metrics relating to cellular radius, concavity and symmetry of the cell nuclei. The results from this analysis may ultimately be leveraged to assist clinicians and health care providers in the early detection and diagnosis of breast cancer in an effort to provide the best possible patient care.
