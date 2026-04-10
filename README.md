The purpose of this repository is to investigate which of four machine learning models is most proficent in predicting if a patient will have diabetes based on a variety of health factors including BMI, age, physical health, high blood pressure, high cholesterol, etc. 

We tested four machine learning models: Logistic Regression, Linear Discriminant Analysis (LDA), Naive Bayes and Neural Networks. 

The dataset was obtained from Kaggle, and was already preprocessed and ready for use. Link to dataset: https://www.kaggle.com/datasets/alexteboul/diabetes-health-indicators-dataset/data

There are three different files in the dataset, each with 22 columns total and 21 feature columns. We have used the second file, which has 70,692 records where the data is evenly split in the diabetes response column between no diabetes, which is denoted as 0, or having prediabetes or diabetes, which is denoted as 1.

The dataset contains 70,692 records with 21 features capturing health indicators, demographics, and lifestyle information. The target variable is Diabetes_binary, a binary indicator where 0 represents no diabetes and 1 represents prediabetes or diabetes. Features include 14 binary variables (high blood pressure, cholesterol, smoking status), 3 ordinal variables (age group, education level, income), and 1 continuous variable (BMI). No missing values remain after preprocessing, and BMI outliers were capped to ensure data quality. Initial insights revealed that roughly 30% of participants have high blood pressure, the average BMI is around 30, and the majority of participants fall within the 45–65 age range. We validated that the dataset is balanced, with 50% of individuals classified as diabetic/prediabetic.

Feature normalization methodology included scaling the BMI column, since this is the only column that is not expressed in the same categorical scale. We used all of the features given in the dataset after scaling, as well. 
Some specific packages we used included pandas, NumPy for data manipulation, scikit-learn for model implementation, preprocessing, train/test splitting, and Matplotlib and Seaborn for visualizations. We evaluated models using accuracy, precision, recall, F1-score and confusion matrices as applicable. Recall will be especially useful in this medical context, as minimizing false negatives, patients with diabetes who are incorrectly predicted as healthy, is critical. 

Each file in this repository is a different machine learning model or the dataset feature normalization preparation, as denoted by the file name. 
The DatasetExploration file is where we did some of our dataset exploration and analysis.
We have also included graphs in each file displaying the overall results of each model's ability to predict relative to one another as well as graphs showing the contribution of each feature to diabetes or no diabetes based on results from each model. 
