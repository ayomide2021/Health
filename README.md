
# Introduction
This project serves as a showcase of my data analysis, visualization, modelling, and machine learning skills, all of which I have acquired through my learning journey in the data analytics track with Python on Udemy. The problem statement for this project is based on an imaginary scenario that I devised after coming across a relevant dataset. My choice of dataset is deliberate, as it aligns with my prior experience in a healthcare setting during my university studies.

In this project, I aim to apply the knowledge and skills I've gained to address this fictional healthcare scenario and demonstrate how data analytics and machine learning can be valuable tools in this context. By doing so, I intend to highlight the practical applications of the techniques I've learned and their relevance in real-world situations.

# Problem Statement
A healthcare solutions provider is seeking to develop a straightforward model for predicting the total costs associated with various health-related factors, including age, illness severity, patient disposition, and the type of treatment administered during a hospital stay. To achieve this, the company's research team has enlisted our analytics team to create, fine-tune, test, and compare several linear regression models. The goal is to identify the best-performing model based on key evaluation metrics, including the root-mean-squared error (RMSE), coefficient of determination (r2), and mean absolute percentage error (MAPE). This project aims to address the company's need for an accurate cost prediction tool, ultimately improving its healthcare services and resource allocation.

# Data source
The dataset used in this project was obtained from an online source on Udemy. I downloaded the dataset in CSV format and subsequently imported it into Python using the Pandas library. The dataset was then subjected to a series of data cleaning, analysis, and visualization steps. In its raw form, the dataset comprised 67,928 rows and 32 columns.
This process of data extraction and preparation forms the foundation for the subsequent data analysis and modelling steps in the project.

# Data Transformation/Cleaning
Data cleaning and transformation were executed within a Jupyter notebook using the Pandas library. To ensure the dataset's integrity, each column was meticulously inspected through a for-loop, confirming the absence of empty cells or errors.
In some columns, categorical variables were present. To make these columns compatible with machine learning algorithms, the categorical variables were converted into numerical floats. This transformation was achieved using a Label Encoder, which assigns a unique numerical label to each category, thereby enabling the inclusion of these features in the modelling process.

By carrying out these data cleaning and transformation steps, the dataset was prepared for subsequent analysis and modelling, ensuring data quality and compatibility with the chosen machine learning techniques.

# Preliminary data exploration
As part of the project, I conducted an extensive Exploratory Data Analysis (EDA) and utilized statistical data visualization techniques to gain insights from the dataset. The key steps in this phase included:
Pairwise Correlations: I calculated pairwise correlations among the various features in the dataset to identify the relationships between them and, in particular, their associations with the dependent variable, "total costs."
Correlation Matrix: To visualize these correlations, I created a correlation matrix and employed a Seaborn heatmap. This heatmap provides a visual representation of the strength and direction of correlations between variables. It is an essential tool for identifying potential predictors of "total costs."
Seaborn lmplot: To further explore and confirm the relationships between the strongest pairs of variables, I used Seaborn's lmplot. This technique allows for a more detailed examination of the correlations and aids in understanding how they may impact "total costs."
By conducting EDA and employing these statistical data visualization methods, I aimed to uncover significant patterns and insights within the dataset, which would be instrumental in constructing and fine-tuning the predictive model for "total costs."

# Data Modelling
The dataset was divided into two subsets, the training set (80%) and the test set (20%), utilizing the train_test_split function from the sklearn.model_selection library. This splitting process ensured that the models would be trained on one subset and evaluated on another. The features were extracted, and labels were assigned for both subsets, resulting in the following:

•	Training Set: Features (X_train) and Labels (y_train)
•	Test Set: Features (X_test) and Labels (y_test)
With the data prepared, three linear models were created, fine-tuned, tested, and compared. These models include:
1.	Simple Linear Regression
2.	Elastic Net
3.	Linear Support Vector Regression
The performance of these models was assessed using specific metrics, which included:
Root-Mean Squared Error (RMSE): A measure of the model's prediction accuracy.
Coefficient of Determination (r2): Indicates the proportion of the variance in the dependent variable that is predictable from the independent variables.
Mean Absolute Percentage Error (MAPE): An evaluation of the accuracy of the model's predictions.
Additionally, the prediction times of these models were recorded and taken into account when selecting the best model for the client. This consideration ensures that not only the predictive accuracy but also the computational efficiency aligns with the client's needs.
By conducting this thorough model comparison and evaluation, we aimed to identify the most suitable model for predicting "total costs" in the healthcare context.

# Analysis
Based on the metrics, the simple linear regression was chosen as the best model for our client as it outperformed the other models in three of four metrics. 

# Conclusions/recommendations

1.	The exploratory data analysis revealed that the length of hospital stay exhibited the most substantial correlation with total costs.
2.	Emergency admissions accounted for over half of the total hospital admissions.
3.	The average length of hospital stay is approximately 5 days.
4.	The choice of the simple linear regression model for our client was made because it outperformed the other models.
5.	While simple linear regression models offer high interpretability and ease of understanding, they tend to be generally less accurate compared to complex models like Random Forest and Decision Trees. Future analyses for our client will target the utilization of more complex models to improve predictive accuracy.
