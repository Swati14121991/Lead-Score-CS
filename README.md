**Case Study: Lead Scoring Problem Statement**

X Education, a provider of online courses for industry professionals, aims to improve its lead conversion process by identifying the most promising leads—those with the highest probability of becoming paying customers.

To achieve this, the company requires a lead scoring model that assigns a numerical score to each lead. A higher score indicates a greater likelihood of conversion, while a lower score suggests a reduced probability. The CEO has set a target lead conversion rate of approximately 80%, making it crucial to develop an efficient and accurate model for lead prioritization.

**Solution Approach**

**Step 1: Data Collection and Understanding**
The dataset was thoroughly analyzed to understand its structure, distribution, and key features.
Initial exploratory analysis was performed to identify patterns, inconsistencies, and potential data quality issues.

**Step 2: Data Cleaning and Preprocessing**
Handling Missing Data:
Variables with a high percentage of missing values were dropped.
Missing numerical values were imputed using median values to ensure data integrity.
Categorical variables were adjusted by creating new classification categories where necessary.
Outlier Treatment:
Outliers were identified and removed to improve model performance and prevent skewed results.

**Step 3: Exploratory Data Analysis (EDA)**
Performed EDA to assess variable distributions, correlations, and relationships between features.
Identified and removed three variables that contained only a single unique value across all rows, as they provided no meaningful information.

**Step 4: Encoding Categorical Variables**
Created dummy variables for categorical features, transforming them into a format suitable for machine learning models.

**Step 5: Splitting the Data for Model Training and Testing**
The dataset was divided into:

70% training data for model development.

30% test data for validation and performance assessment.

**Step 6: Feature Scaling**
Applied Min-Max Scaling to normalize numerical features and ensure consistency across different variables.
Developed an initial statistical model to analyze the impact of each feature on lead conversion.

**Step 7: Feature Selection Using Recursive Feature Elimination (RFE)**
Implemented Recursive Feature Elimination (RFE) to identify and retain the most influential features.
Conducted iterative analysis using P-values and Variance Inflation Factor (VIF) to refine feature selection.
Finalized 12 key features that had the highest impact on conversion probability.
Established an initial assumption: Leads with a probability score ≥ 0.5 were classified as potential conversions (1), while those < 0.5 were labeled as non-converting (0).
Evaluated model performance using Confusion Metrics to measure accuracy, sensitivity, and specificity.

**Step 8: ROC Curve Analysis**
Generated a Receiver Operating Characteristic (ROC) Curve to assess model effectiveness.
The model demonstrated strong predictive performance, with an Area Under the Curve (AUC) score of 95%, confirming its reliability.

**Step 9: Determining the Optimal Probability Cutoff**
Plotted probability curves for Accuracy, Sensitivity, and Specificity to determine the best threshold for lead classification.
The optimal cutoff was identified as 0.3, improving the model’s predictive power.
Key performance metrics at this cutoff:

Accuracy: 87.8%

Sensitivity (Recall): 88.1%

Specificity: 87.6%

The model successfully aligned with the CEO’s 80% target conversion rate, making it highly effective for lead scoring.

**Step 10: Evaluating Precision and Recall Metrics**
Analyzed Precision and Recall to understand the trade-off between capturing true conversions and minimizing false positives.
Computed values:
Precision: 91.6%

Recall: 81.1%

Determined an optimal probability cutoff of 0.35, ensuring a balanced approach between precision and recall.

**Step 11: Model Validation on the Test Set**
Applied the trained model to the test dataset to validate real-world performance.
Evaluated lead conversion probability using Sensitivity and Specificity metrics.
Final test set performance:

Accuracy: 87%
Sensitivity: 84.3%
Specificity: 82.2%


