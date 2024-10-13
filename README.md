# GST Fraud Detection Using Machine Learning

This project focuses on detecting fraudulent transactions in the Goods and Services Tax (GST) system using advanced machine learning techniques. It addresses the critical issue of fraud detection in GST transactions, which is crucial for maintaining the integrity of the tax system and preventing revenue losses.

## Table of Contents
- [Introduction](#introduction)
- [Problem Statement](#problem-statement)
- [Objectives](#objectives)
- [Approach](#approach)
- [Results](#results)
- [Conclusion](#conclusion)
- [Future Work](#future-work)

## Introduction

Fraud detection in GST is a significant challenge due to the increasing incidence of fraudulent activities, including fake invoices, input tax credit (ITC) fraud, and underreporting of sales. Traditional methods often fall short in handling large datasets and recognizing nuanced patterns indicative of fraudulent behavior. This project leverages machine learning techniques to enhance fraud detection capabilities.

## Problem Statement

The dataset consists of 21 features, including the target variable indicating fraudulent or non-fraudulent transactions. A major challenge is the class imbalance within the dataset, where fraudulent cases constitute a very small percentage of the total transactions. This imbalance complicates the prediction of fraudulent activities, as standard classification algorithms may perform poorly on underrepresented classes.

## Objectives

1. Construct a predictive model capable of accurately detecting fraudulent GST transactions.
2. Implement techniques that address the imbalance in the dataset using a custom mathematical approach.
3. Evaluate model performance using metrics tailored for imbalanced data.

## Approach

### Data Preprocessing
- Data cleaning and handling of missing values
- Feature engineering
- Encoding of categorical variables

### Addressing Class Imbalance
- Oversampling techniques (e.g., SMOTE)
- Undersampling of the majority class
- Cost-sensitive learning

### Model Selection and Training
- Algorithms evaluated: Logistic Regression, Decision Trees, Random Forest, XGBoost, LightGBM
- Stratified k-fold cross-validation

### Evaluation Metrics
- Precision
- Recall
- F1-score
- ROC-AUC

## Results

The project compared various models and techniques. Here are the detailed performance metrics for different approaches:

| Model/Approach | Accuracy (%) | Precision (%) | Recall (%) | F1-Score (%) | ROC-AUC (%) |
|----------------|--------------|---------------|------------|--------------|-------------|
| Base Models |
| XGBoost | 98 | 85 | 94 | 89 | 99 |
| Gaussian Naive Bayes | 96 | 74 | 84 | 79 | 96 |
| Under-Sampling |
| XGBoost (Under-Sampling) | 97 | 76 | 100 | 86 | 99 |
| Gaussian Naive Bayes (Under-Sampling) | 96 | 75 | 79 | 77 | 96 |
| Over-Sampling |
| XGBoost (Over-Sampling) | 97 | 78 | 99 | 87 | 99 |
| Gaussian Naive Bayes (Over-Sampling) | 96 | 73 | 89 | 80 | 96 |
| SMOTE |
| XGBoost (SMOTE) | 98 | 83 | 95 | 89 | 99 |
| Gaussian Naive Bayes (SMOTE) | 92 | 54 | 88 | 67 | 94 |

Key findings include:

- XGBoost consistently outperformed other algorithms across various methodologies.
- The base XGBoost model achieved high accuracy (98%) and ROC-AUC (99%).
- Undersampling techniques significantly improved recall, with XGBoost reaching 100% recall.
- SMOTE improved the balance between precision and recall for XGBoost, maintaining high performance across all metrics.

## Conclusion

The study successfully developed a predictive model for fraud detection in GST transactions, effectively addressing the class imbalance issue. The implemented machine learning techniques, particularly XGBoost with resampling methods, demonstrated considerable promise in accurately identifying fraudulent activities. The use of resampling techniques like under-sampling and SMOTE proved effective in improving model performance, particularly in terms of recall and F1-score.

## Future Work

- Explore advanced techniques such as deep learning and ensemble methods
- Integrate real-time data and feedback loops for continuous model improvement
- Adapt the model to evolving fraud patterns
- Further optimize the best-performing models (XGBoost) for deployment in real-world scenarios

## Getting Started

(Add instructions for setting up the project, installing dependencies, and running the code)

## Contributing

(Add guidelines for contributing to the project)

## License

(Specify the license under which this project is released)

## Contact

(Add contact information or links to the project maintainers)
