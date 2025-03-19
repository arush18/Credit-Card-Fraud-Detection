# Credit Card Fraud Detection

## Overview
This project aims to detect fraudulent credit card transactions using machine learning. The dataset used is sourced from Kaggle and contains real-world anonymized credit card transactions labeled as fraudulent or legitimate. 

## Project Structure
```
credit-card-fraud-detection/
│── datasets/              # Contains creditcard.csv (not pushed to repo)
│── results/               # Stores visualizations and model performance metrics
│   ├── visualizations/    # Includes 9 saved graphs plotted in main.ipynb
│── src/                   # Source code
│   ├── main.ipynb         # Jupyter Notebook containing data analysis and model building
│── .gitignore             # Specifies files to be ignored in version control
│── LICENSE.md             # License file
│── README.md              # Project documentation
```

## Dataset
- The dataset is sourced from Kaggle and contains anonymized credit card transaction data.
- It has `284,807` transactions with `492` fraud cases.
- Features include `V1, V2, ... V28` (anonymized principal components), `Time`, and `Amount`.
- Target variable: `Class` (0 = Legitimate, 1 = Fraudulent).

## Data Preprocessing
- Loaded the dataset and checked for missing values.
- Performed exploratory data analysis (EDA) to understand feature distributions.
- Handled class imbalance using techniques like **SMOTE**.

## Data Visualization
Several graphs were generated to explore and analyze the dataset, including:
1. Distribution of transaction amounts.
2. Correlation heatmap of features.
3. Class distribution (imbalanced dataset visualization).
4. Time-based distribution of transactions.
5. Feature importance from trained models.
6. ROC Curve for model evaluation.
7. Precision-Recall Curve.
8. Fraud vs. Non-Fraud transaction distributions.
9. PCA visualization of feature space.

Visualizations are stored in `results/visualizations/`.

## Model Training
- Various machine learning models were trained, including:
  - Logistic Regression
  - Decision Tree
- Evaluation metrics used:
  - **Accuracy, Cross-Val Score, Confusion Matrix**

## Results
- The best-performing model was selected based on **Cross-Val Score**.
- Fraud detection models were tested to minimize false positives and false negatives.

## Installation & Usage
1. Clone the repository:
   ```bash
   git clone https://github.com/arush18/Credit-Card-Fraud-Detection
   ```
2. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```
3. Run the Jupyter Notebook:
   ```bash
   jupyter notebook src/main.ipynb
   ```

## License
This project is licensed under the MIT License. See `LICENSE.md` for details.

## Acknowledgments
- Dataset sourced from Kaggle: [Credit Card Fraud Detection Dataset](https://www.kaggle.com/datasets/mlg-ulb/creditcardfraud)
- Machine learning techniques inspired by various research papers on fraud detection.