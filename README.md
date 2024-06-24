
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


