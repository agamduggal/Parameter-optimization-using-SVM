# Parameter Optimization for SVM on Air Quality Dataset
This repository demonstrates the parameter optimization process for Support Vector Machine (SVM) models using the Air Quality Dataset from the UCI Machine Learning Repository. The dataset contains 9358 instances of hourly averaged responses from an array of 5 metal oxide chemical sensors embedded in an Air Quality Chemical Multisensor Device.

## Dataset Overview
The dataset includes information about air quality measurements with 13 features (after cleaning) sensitive to various air pollutants. The task is a multi-class classification problem to predict the air quality level.

## Dataset Information:
- Instances: 9,358 (after cleaning)
- Features: 13
- Target Variable: Classification of air quality level
- Subject Area: Environment

## Objective
This project focuses on applying Support Vector Machine (SVM) for multi-class classification with parameter optimization to predict air quality levels using sensor data. The goal is to find the optimal parameters that improve the SVM model's performance across 10 different training samples.

## Methodology
### Data Loading and Preprocessing:
- Load the dataset from the UCI repository
- Handle missing values and clean the data
- Prepare features (X) and target (y)

### Train-Test Splits:
- Create 10 different 70-30 train-test splits using different random seeds

### SVM Parameter Optimization:
For each sample (S1-S10):
- Perform 100 iterations of random parameter search
- Test combinations of:
  - Kernel: 'linear', 'poly', 'rbf', 'sigmoid'
  - Nu: [0.1, 1.0]
  - Epsilon: [0.001, 1.0]
- Record the best accuracy and corresponding parameters

### Results Reporting:
- Maintain Table 1 showing comparative performance across all samples
- Generate a convergence graph for the sample with maximum accuracy

### Visualization:
Plot the convergence graph showing how accuracy improves over iterations for the best sample

## Results
Table 1: Comparative performance of Optimized-SVM with different samples

![image](https://github.com/user-attachments/assets/09d0bd55-678e-4603-9d7e-7b3cc52618f7)

Figure 1: Convergence graph of the best SVM

![image](https://github.com/user-attachments/assets/7804770e-a558-4bdb-abe1-32ed0a30316a)


## Conclusion
The SVM parameter optimization process successfully identified optimal hyperparameters for each of the 10 samples. The convergence graph demonstrates how the optimization process progressively found better parameter combinations. The results show that careful parameter tuning can significantly impact SVM performance on air quality classification tasks.
