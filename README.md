# Executive Summary
A healthcare solutions provider is facing challenges in accurately predicting the total costs associated with various health-related factors during hospital stays. These factors include patient age, illness severity, patient disposition, and the type of treatment administered. Accurate cost predictions are crucial for effective resource allocation, financial planning, and improving overall service quality. However, the existing methods for cost prediction are not providing the desired accuracy and reliability, leading to inefficiencies and potential financial losses.
### Key take aways:
•	Among the tested models, the Simple Linear Regression model outperformed the Elastic Net and Linear Support Vector Regression models in terms of predictive accuracy and computational efficiency.

•	Short-Term: Implement the Simple Linear Regression model for cost prediction due to its high performance in our tests and its straightforward nature, which makes it easy to interpret and apply.

•	Long-Term: Explore and utilize more complex models like Random Forest and Decision Trees to improve predictive accuracy in future analyses.

# Business Problem
A fictional healthcare solutions provider needs a robust and accurate model to predict the total costs of hospital stays based on multiple health-related factors. The current methods are inadequate, resulting in suboptimal resource allocation and financial planning. There is a critical need to develop, test, and compare several predictive models to identify the most effective one. This will help the provider enhance its cost prediction capabilities, leading to better financial management and improved healthcare services.

# Objective
The goal is to identify the most accurate cost prediction model to enhance the provider's healthcare services and resource allocation. The goal is broken down into smaller tasks as follows:

•	Develop Multiple Predictive Models: Create and fine-tune different linear regression models, including Simple Linear Regression, Elastic Net, and Linear Support Vector Regression (SVR).

•	Evaluate Model Performance: Assess the models using key evaluation metrics such as Root-Mean Squared Error (RMSE), Coefficient of Determination (r2), and Mean Absolute Percentage Error (MAPE).

•	Compare and Select the Best Model: Identify the best-performing model based on accuracy, computational efficiency, and ease of interpretation.

•	Improve Cost Prediction: Implement the selected model to enhance the accuracy of cost predictions, aiding in better resource allocation and financial planning


# Tech Used
•	Python: Pandas, Matplotlib, Numpy, sklearn


# Data Transformation
Data cleaning and transformation were executed within a Jupyter Notebook using the Pandas library. To ensure the dataset's integrity, each column was meticulously inspected through a for-loop, confirming the absence of empty cells or errors.
In some columns, categorical variables were present. To make these columns compatible with machine learning algorithms, the categorical variables were converted into numerical floats. This transformation was achieved using a Label Encoder, which assigns a unique numerical label to each category, thereby enabling the inclusion of these features in the modelling process.


# Exploratory Data Analysis (EDA)
As part of the project, I conducted an extensive Exploratory Data Analysis (EDA) and utilized statistical data visualization techniques to gain insights from the dataset. The key steps in this phase included:
Pairwise Correlations: I calculated pairwise correlations among the various features in the dataset to identify the relationships between them and, in particular, their associations with the dependent variable, "total costs."
Correlation Matrix: To visualize these correlations, I created a correlation matrix and employed a Seaborn heatmap. This heatmap provides a visual representation of the strength and direction of correlations between variables. It is an essential tool for identifying potential predictors of "total costs."
Seaborn lmplot: To further explore and confirm the relationships between the strongest pairs of variables, I used Seaborn's lmplot. This technique allows for a more detailed examination of the correlations and aids in understanding how they may impact "total costs."
By conducting EDA and employing these statistical data visualization methods, I aimed to uncover significant patterns and insights within the dataset, which would be instrumental in constructing and fine-tuning the predictive model for "total costs."

## Explore the type of admission
![O1](https://github.com/ayomide2021/Health/assets/83126882/d1ab76df-59f1-46d8-8569-53d7fffba43f)


## Explore APR Risk of Mortality
![O2](https://github.com/ayomide2021/Health/assets/83126882/95b4212e-26aa-4a9f-8ba3-6eac5913aa28)

## Explore the distribution of total costs and length of stay in hospitals
![O3](https://github.com/ayomide2021/Health/assets/83126882/e05554f9-cef8-4432-ace8-66b98387c704)

## Total Costs Distribution
![O4](https://github.com/ayomide2021/Health/assets/83126882/c28e2792-d967-468b-b9f6-9c06eeae2747)

##  Build a correlation matrix with the numeric data columns
![O5](https://github.com/ayomide2021/Health/assets/83126882/434fbe3f-77ad-4f67-900a-72af4ab4dc3c)

# Methodology

## Data Preparation
•	The dataset was divided into training (80%) and test (20%) sets using the train_test_split function from the sklearn.model_selection library.

•	Features and labels were extracted and assigned for both subsets.

## Model Development:
Three linear regression models were created, fine-tuned, tested, and compared:

•	Simple Linear Regression

•	Elastic Net

•	Linear Support Vector Regression (SVR)

## Model Evaluation:
Performance of the models was assessed using key metrics:

•	Root-Mean Squared Error (RMSE): Measures the model's prediction accuracy.

•	Coefficient of Determination (r2): Indicates the proportion of variance in the dependent variable predictable from the independent variables.

•	Mean Absolute Percentage Error (MAPE): Evaluates the accuracy of the model's predictions.

Prediction times were recorded to ensure that computational efficiency met the client's requirements.


# Results and Insights

## Findings
•	The exploratory data analysis identified that the length of hospital stay had the most substantial correlation with total costs.

•	Emergency admissions constituted over half of the total hospital admissions.

•	The average length of hospital stay was approximately five days.

## Model Comparison and Selection
•	Among the tested models, the Simple Linear Regression model outperformed the Elastic Net and Linear Support Vector Regression models in terms of predictive accuracy and computational efficiency.

•	Despite the simplicity of the Simple Linear Regression model, which offers high interpretability and ease of understanding, it generally tends to be less accurate than more complex models such as Random Forest and Decision Trees.

# Recommendations
•	Short-Term: Implement the Simple Linear Regression model for cost prediction due to its high performance in our tests and its straightforward nature, which makes it easy to interpret and apply.

•	Long-Term: Explore and utilize more complex models like Random Forest and Decision Trees to improve predictive accuracy in future analyses.
By implementing these recommendations, the healthcare provider can achieve better cost predictions, enhancing resource allocation and overall service quality.

# Next Steps
Implementation of Random Forest and Decision Trees to improve predictive accuracy in future analyses. 

