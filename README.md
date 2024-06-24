

# Learning Agency Lab - Automated Essay Scoring 2.0 
In this project,I used to develop and evaluate models for automated essay scoring: Quadratic Weighted Kappa (QWK) Calculation. This technique enhanced the model's accuracy and reliability, making the automated scoring system more effective.

# 1. Quadratic Weighted Kappa Calculation
Quadratic Weighted Kappa (QWK) is a statistical measure used to evaluate the agreement between two sets of categorical data, particularly in contexts requiring high inter-rater reliability. It ranges from -1 (complete disagreement) to 1 (perfect agreement), with 0 indicating no agreement beyond chance. In essay scoring, QWK compares predicted scores from the model with actual human-assigned scores, providing a measure of the model's prediction accuracy.

# The QWK calculation involves:

Constructing a Confusion Matrix: This matrix represents the frequency of observed scores versus predicted scores.
Creating a Weight Matrix: The weight matrix is based on the squared differences between observed and predicted scores.
Normalizing the Expected Matrix: This accounts for the agreement by chance.
Calculating the Kappa Score: The kappa score is computed using the formula:

​![image](https://github.com/RobinaMirbahar/Kaggle-competition/assets/60986830/23c27b89-8f47-4eeb-8208-465db5da3da3)

 
​where 𝑂 is the observed matrix, 𝐸 is the expected matrix, and 𝑤 is the weight matrix. This metric is crucial for assessing the effectiveness of different models and ensuring they provide reliable predictions.

# Acknowledgments
Vanderbilt University and the Learning Agency Lab would like to thank the Bill & Melinda Gates Foundation, Schmidt Futures, and Chan Zuckerberg Initiative for their support in making this work possible.

#🔗 Links for competition
[(https://www.kaggle.com/competitions/learning-agency-lab-automated-essay-scoring-2)]


## Description of the Project


**Introduction:**
Hello! Today, we're diving into a script that demonstrates the development of an automated essay scoring system using machine learning techniques. Let's walk through the key steps and insights gained from the process.

**1. Data Loading and Preparation:**
The script begins by loading essential datasets: the training data containing essays (`full_text`) and their corresponding scores (`score`), alongside the test data which lacks the scores. This is critical as it sets the foundation for training and evaluating our model.

**2. Data Integrity Check:**
We ensure data integrity by checking for missing values in the training data. It's important to start with clean, complete datasets to avoid biases or errors in our analysis.

**3. Splitting the Data:**
To assess the model's performance accurately, we split the training data into training and validation sets using `train_test_split()`. This approach allows us to train the model on one subset and validate it on another, ensuring that our model generalizes well to unseen data.

**4. Feature Extraction with TF-IDF:**
Textual data (`full_text`) is converted into numerical features using `TfidfVectorizer`. This step transforms essays into a matrix of TF-IDF (Term Frequency-Inverse Document Frequency) features, which captures the importance of words within each essay relative to the entire dataset.

**5. Model Training - Ridge Regression:**
We employ a Ridge Regression model (`Ridge`) from the `sklearn` library. Ridge Regression is chosen for its ability to handle multicollinearity in data and prevent overfitting by adding a penalty to the magnitude of coefficients. This regularization technique enhances the model's stability and performance.

**6. Evaluation Metric - Quadratic Weighted Kappa (QWK):**
To evaluate the model's accuracy in predicting essay scores, we use the Quadratic Weighted Kappa (QWK) score. This metric measures the agreement between predicted and actual scores, providing a robust assessment of our model's performance in handling the complexity of essay grading.

**7. Model Evaluation and Prediction:**
After training the model on the training set, we predict essay scores on the validation set (`val_data`). These predictions are then evaluated using the QWK score function (`quadratic_weighted_kappa()`), ensuring that our model aligns closely with human-assigned scores.

**8. Generating Predictions for Submission:**
With validated model performance, we proceed to predict essay scores for the test dataset (`test_df`). These predictions are rounded to integers and formatted into a submission file (`submission.csv`), which adheres to the competition or project requirements.

**Conclusion:**
In conclusion, this script exemplifies a systematic approach to automated essay scoring using machine learning. By leveraging techniques like Ridge Regression and evaluating with QWK, we create a robust model capable of efficiently and accurately assessing essays based on textual content. Such systems not only alleviate the workload of educators but also provide timely and consistent feedback to students, enhancing the learning experience across diverse educational settings.
