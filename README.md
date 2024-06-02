# Heart Disease Detection Using Classification Methods

## Abstract
Heart diseases remain a prominent cause of death worldwide. This project addresses the necessity for solutions that can identify individuals at risk of heart disease promptly and precisely. Leveraging data visualization techniques and machine learning models, a reliable and efficient tool was developed to assist healthcare professionals in this task. Beginning with detailed Exploratory Data Analysis (EDA), visualizations were employed to unravel complex patterns within the Cleveland Heart Disease dataset. Subsequently, multiple classification algorithms were trained and evaluated using various metrics. The objective is to identify the most effective method for accurately detecting heart disease. The appropriate classification model will enable timely diagnosis and treatment of heart diseases.

## Steps to Simulate the Project:

1. Open the jupyter notebook, named "Heart_Disease_Detection.ipynb".
2. Make sure to download the dataset from https://doi.org/10.24432/C52P4X and save as "heart_disease_uci.csv" (Also uploaded in this repository).
3. Change the path location of the data file in the jupyter notebook.
4. Before running the code make sure to install all the prerequisites as mentioned below.
5. Run all the code segments in the jupyter notebook to preprocess, visualize and transform the data. Finally, run the code segments to train the classification models and evaluate their performance.

## Prerequisites

Make sure you have the following installed:

- Jupyter Notebook with Python-3 kernel
- Required libraries (e.g. 'numpy', 'pandas', 'scikit-learn', 'seaborn', 'matplotlib', 'xgboost')

## Table of Contents
1. [Introduction](#introduction)
2. [Previous Work](#previous-work)
3. [Methodology](#methodology)
    - [Dataset](#dataset)
    - [Computational Resources and Tools Used](#computational-resources-and-tools-used)
    - [Exploratory Data Analysis (EDA)](#exploratory-data-analysis-eda)
    - [Data Transformation for Modeling](#data-transformation-for-modeling)
4. [Classification Modeling](#classification-modeling)
5. [Results](#results)
6. [Conclusion](#conclusion)
7. [References](#references)

## Introduction
Cardiovascular diseases, particularly heart disease, stand out as a leading cause of death across the world. Heart disease often progresses silently, with symptoms appearing only in advanced stages. Early detection and accurate risk assessment are crucial in preventing and managing heart diseases. This research aims to use data visualization techniques and machine learning models to develop a reliable and efficient tool that can assist healthcare professionals in identifying individuals at risk of heart disease, ultimately leading to improved patient outcomes and reduced healthcare costs.

## Previous Work
In medical science, various machine learning algorithms are actively utilized for data analysis and advancement. Recent research in healthcare has showcased instances of machine learning utilization, such as identifying COVID-19 through X-rays, detecting tumors via MRIs, and predicting cardiac issues. Studies have employed algorithms like Random Forest, Decision Tree Classifier, Multilayer Perceptron, and XGBoost to predict cardiovascular diseases, demonstrating the efficacy of these models in clinical settings.

## Methodology

### Dataset
The Cleveland Heart Disease dataset, available in the UCI Machine Learning Repository, was used for this research. The dataset consists of 76 attributes, but we focused on a subset of 13 features used in previous studies. These features include age, sex, chest pain type (cp), resting blood pressure (trestbps), serum cholesterol (chol), fasting blood sugar (fbs), maximum heart rate achieved (thalach), exercise-induced angina (exang), ST depression (oldpeak), slope of the peak exercise (slope), number of major vessels (ca), and types of defect (thal). The target variable, `disease_present`, was mapped to binary values indicating the absence or presence of heart disease.

### Computational Resources and Tools Used
The project was implemented using Python within a Jupyter Notebook environment, utilizing essential libraries such as Matplotlib, Seaborn, Scikit-learn, NumPy, and Pandas. No extra computational resources were required beyond standard CPU cores.

### Exploratory Data Analysis (EDA)
The project commenced with loading and understanding the dataset. Missing values were handled appropriately, and features were visualized using bar charts, box plots, violin plots, and pair plots to uncover complex patterns and relationships within the data.

### Data Transformation for Modeling
Categorical features were label encoded using Scikit-learn's `LabelEncoder`. Features like 'cp', 'restecg', 'slope', 'thal', 'fbs', and 'exang' were converted into numerical representations, ensuring they were appropriately represented for machine learning models.

## Classification Modeling
For predicting heart disease, three machine learning models were used: Logistic Regression, XGBoost, and Support Vector Machine (SVM). Each model was trained and evaluated on the dataset. The data was split into training and testing sets, with standard scaling applied for uniformity across features.

### XGBoost
XGBoost is a scalable and distributed gradient-boosted decision tree (GBDT) machine learning framework. We used the `XGBClassifier` for binary classification with default parameters and trained it on the heart disease dataset.

### SVM
Support Vector Machine (SVM) is a supervised learning algorithm suitable for classification tasks. The SVM model was trained using an RBF kernel with default parameters.

### Logistic Regression
Logistic Regression is a statistical method used for binary classification problems. The model was trained with default parameters, utilizing predictor variables such as age, cholesterol levels, exercise habits, and chest pain type.

## Results
The models were evaluated using metrics such as accuracy, precision, recall, and F1 score. SVM demonstrated the highest accuracy at 80%, followed by XGBoost at 78%, and Logistic Regression at 77%. SVM's higher recall (83%) suggests its effectiveness in capturing individuals with heart disease. Precision was consistent across models at 84%, resulting in fewer false positives. The F1 score for SVM was 84%, indicating a good balance between capturing disease cases and minimizing false positives.

| Model                | Accuracy | Precision | Recall | F1 Score |
|----------------------|----------|-----------|--------|----------|
| Logistic Regression  | 77%      | 84%       | 78%    | 81%      |
| XGBoost              | 78%      | 84%       | 78%    | 81%      |
| SVM                  | 80%      | 84%       | 83%    | 84%      |

## Conclusion
Support Vector Machine (SVM) emerged as the most accurate model for detecting heart disease, showcasing superior performance in metrics such as recall and F1 score. While XGBoost and Logistic Regression also demonstrated competitive performance, SVM's precision and recall make it a robust choice for early and accurate heart disease detection. Future work could involve fine-tuning the parameters and exploring other classification techniques to further enhance model performance.

## References
1. Pavlova, A. I. (2023). Application of Machine Learning Algorithms for Heart Disease Prediction. Siberian Journal of Life Sciences and Agriculture, 15(3), 475-496. [DOI](https://doi.org/10.12731/2658-6649-2023-15-3-475-496)
2. Ramakrishnan, S., & Mahesh, B. (2023). Heart Disease Prediction Using Machine Learning. International Journal of Engineering Technology and Management Sciences, 7(6). [DOI](https://doi.org/10.46647/ijetms.2023.v07i06.027)
3. Detrano, R., Janosi, A., Steinbrunn, W., Pfisterer, M., Schmid, J.-J., Sandhu, S., Guppy, K. H., Lee, S., & Froelicher, V. (1989). International application of a new probability algorithm for the diagnosis of coronary artery disease. The American Journal of Cardiology, 64(5), 304–310. [DOI](https://doi.org/10.1016/0002-9149(89)90524-9)
4. Ayatollahi, H., Gholamhosseini, L., & Salehi, M. (2019). Predicting coronary artery disease: A comparison between two data mining algorithms. BMC Public Health, 19(1), 448–448. [DOI](https://doi.org/10.1186/s12889-019-6721-5)
5. Nashif, S., Raihan, M.R., Islam, M.R., & Imam, M.H. (2018). Heart Disease Detection by Using Machine Learning Algorithms and a Real-Time Cardiovascular Health Monitoring System. World Journal of Engineering and Technology, 6, 854-873. [Link](https://www.scirp.org/journal/paperinformation.aspx?paperid=88650)
6. Liu, X., Wang, X., Su, Q., Zhang, M., Zhu, Y., Wang, Q., & Wang, Q. (2017). A Hybrid Classification System for Heart Disease Diagnosis Based on the RFRS Method. Computational and Mathematical Methods in Medicine, 2017, 8272091–11. [DOI](https://doi.org/10.1155/2017/8272091)
