# Task 4 - Classification with Logistic Regression

## 📌 Project Overview

This project is part of my AI & ML Internship Task 4.

The objective is to build a binary classification model using Logistic Regression and evaluate its performance using multiple classification metrics.

The Breast Cancer Wisconsin dataset was used for this task.

## 🎯 Objectives

- Prepare a binary classification dataset.
- Split the data into training and testing sets.
- Standardize numerical features.
- Train a Logistic Regression classifier.
- Evaluate the classifier using a confusion matrix.
- Calculate precision and recall.
- Calculate ROC-AUC.
- Plot the ROC curve.
- Tune the classification threshold.
- Understand the sigmoid function.

## 🛠️ Tools & Technologies

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- Google Colab
- GitHub

## 📊 Dataset

The Breast Cancer Wisconsin dataset was used.

The target variable is `diagnosis`:

- `0` = Benign
- `1` = Malignant

The dataset contains numerical measurements describing characteristics of cell nuclei.

The `id` column was removed because it is an identifier rather than a predictive feature.

The empty `Unnamed: 32` column was also removed.

## 🔧 Preprocessing

The following preprocessing steps were performed:

1. Removed unnecessary identifier and empty columns.
2. Encoded the diagnosis column into binary values.
3. Split the dataset into training and testing sets.
4. Used stratified splitting to preserve the class distribution.
5. Standardized the features using `StandardScaler`.

## 🤖 Logistic Regression

A Logistic Regression classifier was trained using the standardized training data.

The model was then used to predict both:

- Class labels
- Probability of the positive class

## 📈 Model Evaluation

At the default classification threshold of 0.50:

| Metric | Score |
|---|---:|
| Accuracy | 96.49% |
| Precision | 97.50% |
| Recall | 92.86% |
| ROC-AUC | 99.60% |

The ROC-AUC score of 0.9960 indicates excellent discrimination between benign and malignant cases.

## 🔲 Confusion Matrix

A confusion matrix was created to identify:

- True Positives
- True Negatives
- False Positives
- False Negatives

This helps evaluate the types of classification errors made by the model.

## 📉 ROC Curve

A ROC curve was plotted using the predicted probabilities.

The ROC-AUC score was 0.9960.

## 🎚️ Threshold Tuning

Different classification thresholds were tested:

| Threshold | Precision | Recall |
|---:|---:|---:|
| 0.30 | 97.62% | 97.62% |
| 0.40 | 97.56% | 95.24% |
| 0.50 | 97.50% | 92.86% |
| 0.60 | 100.00% | 90.48% |
| 0.70 | 100.00% | 90.48% |

A threshold of 0.30 was selected for this project because it provided a strong balance between precision and recall and increased recall compared with the default threshold.

## 🧮 Sigmoid Function

Logistic Regression uses the sigmoid function to convert the model's output into a probability between 0 and 1.

The sigmoid function is:

σ(z) = 1 / (1 + e^(-z))

The probability is then compared with a classification threshold to determine the predicted class.

## 💡 Key Learnings

- Logistic Regression can be used for binary classification.
- Feature standardization is useful when input features have different scales.
- Precision and recall measure different aspects of classification performance.
- ROC-AUC evaluates how well the model separates the two classes across thresholds.
- Changing the classification threshold changes the balance between precision and recall.
- The sigmoid function converts the model output into a probability.

## 📁 Project Files

- `Task_4_Logistic_Regression.ipynb` - Complete analysis and implementation.
- `data.csv` - Dataset used for the project.
- `README.md` - Project documentation.

## ✅ Conclusion

The Logistic Regression classifier achieved strong performance on the test dataset, with 96.49% accuracy, 97.50% precision, 92.86% recall, and a ROC-AUC of 0.9960 at the default threshold.

Threshold tuning showed that a threshold of 0.30 improved recall to 97.62% while maintaining precision at 97.62%.

The project demonstrates the complete workflow of a binary classification problem, from preprocessing and standardization through model training, evaluation, ROC analysis, and threshold selection.
