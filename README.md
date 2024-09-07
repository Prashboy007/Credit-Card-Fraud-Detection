
# Credit Card Fraud Detection

## Overview

This project focuses on detecting fraudulent credit card transactions using machine learning. With the increasing volume of online transactions, it is crucial to have effective systems in place to identify and prevent fraudulent activities. This project utilizes a dataset from Kaggle and applies various machine learning algorithms to predict whether a given transaction is fraudulent.

## Table of Contents

- [Dataset](#dataset)
- [Installation](#installation)
- [Project Structure](#project-structure)
- [Data Preprocessing](#data-preprocessing)
- [Modeling](#modeling)
- [Evaluation](#evaluation)
- [Results](#results)
- [Contributing](#contributing)
- [License](#license)

## Dataset

The dataset used in this project is sourced from [Kaggle](https://www.kaggle.com/mlg-ulb/creditcardfraud). It contains transactions made by credit cards in September 2013 by European cardholders. This dataset presents transactions that occurred over two days, where we have 492 frauds out of 284,807 transactions. The dataset is highly imbalanced, with the positive class (frauds) accounting for 0.172% of all transactions.

### Features:

- **V1 to V28**: Principal components obtained with PCA
- **Time**: The seconds elapsed between this transaction and the first transaction in the dataset
- **Amount**: Transaction amount
- **Class**: 1 for fraudulent transactions, 0 otherwise

## Installation

1. **Clone the repository**:
    ```bash
    git clone https://github.com/yourusername/credit-card-fraud-detection.git
    cd credit-card-fraud-detection
    ```

2. **Create a virtual environment**:
    ```bash
    python -m venv env
    source env/bin/activate  # On Windows use `env\Scripts\activate`
    ```

3. **Install the required packages**:
    ```bash
    pip install -r requirements.txt
    ```




## Data Preprocessing

The data preprocessing steps include:

1. **Handling Imbalanced Data**: Since the dataset is highly imbalanced, techniques like under-sampling, over-sampling, and SMOTE were considered to balance the dataset.
2. **Scaling Features**: Features like `Amount` were scaled using standardization to improve model performance.
3. **Splitting Data**: The dataset was split into training and testing sets using an 80-20 ratio.

## Modeling

Several machine learning algorithms were tested for this project, including:

- **Logistic Regression**
- **Random Forest**
- **Support Vector Machine (SVM)**
- **XGBoost**

The models were trained using the preprocessed data, and their performance was evaluated using various metrics.

## Evaluation

The models were evaluated based on the following metrics:

- **Accuracy**: The proportion of correctly classified transactions.
- **Precision**: The number of true positives divided by the sum of true and false positives.
- **Recall**: The number of true positives divided by the sum of true positives and false negatives.
- **F1-Score**: The harmonic mean of precision and recall.
- **ROC-AUC**: The Area Under the Receiver Operating Characteristic Curve, which provides a single measure of the model's performance.

## Results

The best-performing model was the Random Forest, which achieved the following results on the test set:

- **Accuracy**: 99.93%
- **Precision**: 90.00%
- **Recall**: 85.00%
- **F1-Score**: 87.40%
- **ROC-AUC**: 98.70%

## Contributing

Contributions are welcome! If you find any issues or want to contribute to the project, feel free to submit a pull request or open an issue.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
