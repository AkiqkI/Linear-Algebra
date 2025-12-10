# Customer Analysis & Data Privacy for an Insurance company

## Project Overview

This project explores the application of linear algebra and machine learning techniques to a synthetic insurance dataset. The primary goal is to address several business challenges for the "Sure Tomorrow" insurance company, including customer segmentation, benefit prediction, and data privacy protection, all while maintaining model performance.

## Key Features

*   **Customer Similarity:** Identifying similar customers using k-Nearest Neighbors (kNN) with various scaling and distance metrics.
*   **Benefit Prediction (Classification):** Predicting whether a customer is likely to receive an insurance benefit using a kNN classifier and comparing its performance against a dummy model.
*   **Benefit Prediction (Regression):** Developing a custom Linear Regression model to predict the number of insurance benefits a customer is likely to receive.
*   **Data Obfuscation for Privacy:** Implementing and analytically proving a data transformation method (multiplying features by an invertible matrix) to protect client data without impacting the performance of linear regression models.

## Tasks Covered

### Task 1: Similar Customers
Developed a procedure to find k-nearest neighbors for a given customer, exploring the impact of data scaling (MaxAbsScaler) and distance metrics (Euclidean, Manhattan). Demonstrated that scaling is crucial for meaningful similarity calculations, while the choice of metric had a minimal effect.

### Task 2: Is Customer Likely to Receive Insurance Benefit?
Built and evaluated a kNN-based classifier to predict if a customer receives *any* insurance benefit (binary classification). Performance was measured using F1-score and compared against a random dummy model. Scaling proved decisive, significantly boosting F1-score from ~0.58 to ~0.96.

### Task 3: Predicting Number of Benefits (Regression)
Implemented a custom Linear Regression model to predict the *number* of insurance benefits. The model's performance (RMSE, R²) was evaluated on both scaled and unscaled data, proving that linear regression is invariant to feature scaling.

### Task 4: Obfuscating Data
Created a data transformation algorithm using an invertible matrix to obfuscate personal data (`gender`, `age`, `income`, `family_members`). Analytically and computationally proved that this method protects data without degrading the performance (RMSE, R²) of linear regression models.

## Technologies Used

*   Python
*   Pandas (for data manipulation)
*   NumPy (for numerical operations and linear algebra)
*   Scikit-learn (for kNN, scaling, and metrics)
*   Matplotlib & Seaborn (for data visualization - though not extensively used in the final notebook, pairplots were generated for EDA)

## Conclusion

This project demonstrates that machine learning can be effectively applied to real-world insurance tasks, from customer analysis to benefit prediction. Crucially, it shows how data privacy can be maintained through linear data obfuscation techniques without compromising the quality of linear regression models. Scaling is highlighted as a critical preprocessing step for distance-based algorithms like kNN, while linear regression models are shown to be robust to feature scaling and invertible linear transformations.