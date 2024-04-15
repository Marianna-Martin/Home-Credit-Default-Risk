# My First ML Project-journal
### 1.What is the difference in  significance between taking mean ,median,mode of a datas/which of them should i use for HomeCredit Default risk prediction ML model?
For HomeCredit default risk prediction ML models, it's common to use a combination of mean, median, and mode, depending on the specific features and characteristics of your dataset. Here's how you can use each measure:

1. **Mean**: 
   - The mean can be useful for features where the average value provides meaningful information about the borrower's financial situation, such as average income or average expenses.
   - However, be cautious when using the mean for features that are sensitive to outliers, as extreme values can skew the mean and potentially impact the model's performance.

2. **Median**:
   - The median is more robust to outliers compared to the mean and can be particularly useful for features with skewed distributions or when dealing with datasets containing outliers.
   - For features where the central tendency is more accurately represented by the middle value rather than the average, the median can provide a more stable measure.

3. **Mode**:
   - The mode can be useful for categorical features or features with discrete values, such as loan purpose or payment frequency.
   - Identifying the most common category or value can provide insights into the prevalent characteristics of borrowers and help identify patterns associated with default risk.

In summary, there isn't a one-size-fits-all answer, and the choice of measure depends on the specific features and characteristics of your dataset. It's common practice to explore and analyze the data using various statistical measures, including mean, median, and mode, to gain a comprehensive understanding of the data distribution and identify relevant patterns for predicting default risk.

Additionally, when building ML models for default risk prediction, feature engineering, and selecting relevant features are critical. Consider using domain knowledge and exploring different feature transformations and combinations to improve the predictive performance of your model.

***Used to make multiple values of SK_ID_BUREAU in bureau and bureau_balance into one. I will be using average as it gives a better idea on the nature of the customer.***
# _______________________________________________________________________________________________________________________________________________________________________________________________________________________#### 2.difference between one hot encoding and label encoding
One-hot encoding and label encoding are both techniques used to convert categorical variables into numerical format for machine learning algorithms. However, they differ in their approach and the type of output they produce.

1. **One-Hot Encoding**:
   - In one-hot encoding, each category in the categorical variable is represented by a binary vector.
   - The binary vector has a length equal to the number of unique categories in the variable.
   - Only one position in the binary vector is set to 1, indicating the presence of the category, while all other positions are set to 0.
   - One-hot encoding creates binary features for each category, resulting in a sparse matrix where most values are 0.
   - One-hot encoding is suitable for categorical variables with no ordinal relationship between categories or when the number of categories is relatively small.
   - Example: 
     - Original categories: ['Red', 'Green', 'Blue']
     - One-hot encoded representation:
       - 'Red': [1, 0, 0]
       - 'Green': [0, 1, 0]
       - 'Blue': [0, 0, 1]

2. **Label Encoding**:
   - In label encoding, each category in the categorical variable is mapped to an integer value.
   - The categories are assigned integer labels based on their order of appearance or sorted order.
   - Label encoding results in a single numerical feature, where each category is represented by a unique integer.
   - Label encoding assumes an ordinal relationship between categories, which may not always be appropriate.
   - Label encoding is suitable for ordinal categorical variables where the categories have a meaningful order.
   - Example:
     - Original categories: ['Low', 'Medium', 'High']
     - Label encoded representation:
       - 'Low': 0
       - 'Medium': 1
       - 'High': 2

In summary, the main difference between one-hot encoding and label encoding lies in the representation of categorical variables: one-hot encoding creates binary features for each category, while label encoding assigns integer labels to categories. The choice between these techniques depends on the nature of the categorical variable and the requirements of the machine learning algorithm being used.

## **3.Difference between regression and classification.**
Regression and classification are two fundamental types of supervised machine learning tasks, but they have different objectives and output types. Here's a breakdown of the key differences between them:

1. **Objective:**
   - Regression: In regression, the goal is to predict a continuous target variable(variable that can take on an infinite number of values within a certain range). The output is a real-valued number that represents a quantity, such as price, temperature, or length. Regression models aim to find the relationship between input features and the target variable, allowing predictions of unseen data points.
   - Classification: In classification, the goal is to predict the category or class to which a data point belongs. The output is a discrete label or class that represents a category, such as "spam" or "not spam," "cat" or "dog," or "positive" or "negative." Classification models learn to distinguish between different classes based on input features.
3. **Examples:**
   - Regression: Predicting house prices based on features like size, location, and number of bedrooms; forecasting stock prices based on historical data; estimating the temperature based on weather variables.
   - Classification: Classifying emails as spam or not spam based on their content; recognizing handwritten digits (0-9) in images; diagnosing diseases based on patient symptoms.

In summary, regression is used to predict continuous numerical values, while classification is used to predict discrete class labels. The choice between regression and classification depends on the nature of the target variable and the problem domain.

## 4.

