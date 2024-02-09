# BCW-Diagnostic-PCA-Bayes
The aim of this work is to implement an efficient predictor using samples of information from both classes (malignant and benign). The presented approach aims to enhance the capability of making precise distinctions between the two types, thereby contributing to diagnosis with higher accuracy.

The database Breast Cancer Wisconsin (Diagnostic) [1] consists of 32 columns, where column 1 represents the ID associated with each data example, column 2 represents the diagnosis (malignant or benign), and columns 3 to 32 are occupied with real values calculated for each cell nucleus, including measurements related to: radius (mean of distances from the center of the nucleus to points on the perimeter), texture (standard deviation of gray-scale values), perimeter, area, smoothness (local variation in radius lengths), compactness (calculated as (perimeter^2 / area - 1.0)), concavity (severity of concave portions of the contour), concave points (number of concave portions of the contour), symmetry, and fractal dimension ("coastline approximation" - 1).
The dataset comprises a total of 569 examples, each labeled as malignant or benign based on the cellular characteristics of breast cancer nuclei. The dataset allows potential classification of cancer subtypes using only cellular data, without prior biological knowledge. All values are recorded with 4 digits, and there are no missing values for attributes.

In the particular case of a Bayes classifier for two classes (M=2), also known as binary hypothesis, the algorithm naturally adapts to situations where there are two distinct categories, such as correct/incorrect.

![image](https://github.com/Andrei-AlexandruRusu/BCW-Diagnostic-PCA-Bayes/assets/92977944/176da142-e692-42c2-a120-c05b45dd33bd) 
         
The Bayes decision rule [2]

We assume a set of N vectors, where N1 belong to class ω1 and N2 belong to class ω2. P(ω1) and P(ω2) are the prior probabilities, μ1 and μ2 are the mean vectors, and Σ1 and Σ2 are the covariance matrices of the two classes.

Bayes Classifier has proved to have a good performance on an imbalanced dataset (with proportions of 63% benign and 37% malignant). I believe that data preprocessing through normalization and dimensionality reduction played an essential role in achieving these results. In the case of the 20% testing set, we achieved the highest score (97.4%) with a number of 7 principal components, while for all other configurations, we obtained a score of at least 93.7%.

Resources : 

  [1] Wolberg,William, Mangasarian,Olvi, Street,Nick, and Street,W.. (1995). Breast Cancer Wisconsin
(Diagnostic). UCI Machine Learning Repository. https://doi.org/10.24432/C5DW2B

  [2] V. Neagoe, Neural Networks for Data Exploration, MatrisRom, Bucharest, 2018.
