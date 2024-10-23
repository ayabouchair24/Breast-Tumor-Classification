# Breast-Tumor-Classification

## Overview
This project was developed as part of the Pinktober datathon challenge. The task was to build a machine learning model that predicts whether a breast tumor is benign or malignant based on a set of extracted features such as cell size, texture, and shape.

The goal was to create a robust classification model that could achieve high accuracy and an optimized F1 score to balance precision and recall, crucial for medical diagnosis scenarios.

## Dataset
The dataset consists of features related to breast tumors:
- **Features**: Various metrics related to tumor characteristics, such as cell size, texture, and shape.
- **Target**: Binary classification of tumor diagnosis (Malignant (M) or Benign (B)).

The data was preprocessed and split into training and testing sets. SMOTE was applied to handle class imbalance between benign and malignant cases.

## Approach
To tackle this problem, an ensemble learning approach was used via a **Voting Classifier** that combines:
- **Support Vector Machine (SVM)**
- **Logistic Regression**
- **Random Forest**

### Steps:
1. **Data Preprocessing**: Standardization of features and handling of class imbalance using SMOTE.
2. **Modeling**: A voting classifier was used to combine SVM, Logistic Regression, and Random Forest models.
3. **Hyperparameter Tuning**: I applied GridSearchCV to optimize the hyperparameters of the models, especially for the SVM model, to improve performance.
4. **Evaluation**: The model was evaluated using F1 score and accuracy metrics on a validation set.

## Files in this Repository
- `notebook.ipynb`: Contains the code for data preprocessing, model building, training, evaluation, and submission.
- `train_data.csv`: Training data.
- `test_data.csv`: Test data.
- `submissionfinal.csv`: Submission file with predicted tumor classifications for the test dataset.

## Results
- **F1 Score on validation set**: `0.9777`

## Model
The final model selected was a Voting Classifier with soft voting, which used:
- **SVM**: Optimized using GridSearchCV to tune parameters like `C` and `gamma`.
- **Logistic Regression**: Default configuration.
- **Random Forest**: Default configuration.

## Usage
1. Clone the repository:
    ```bash
    git clone https://github.com/ayabouchair24/Breast-Tumor-Classification.git
    ```
2. Install required packages:
    ```bash
    pip install -r requirements.txt
    ```
3. Run the Jupyter notebook to see the full pipeline:
    ```bash
    jupyter notebook tumor-classification-final.ipynb
    ```

## Submission
The final model's predictions were saved as `submissionfinal.csv`, ready for submission.

## License
This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Acknowledgments
This project was developed as part of a datathon challenge focused on using machine learning to assist in medical diagnosis.
