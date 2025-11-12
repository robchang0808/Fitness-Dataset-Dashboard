# Fitness Dataset Dashboard
This interactive dashboard explores the Activity and Nutrition Quality Dataset from Kaggle (referred to as "fitness_dataset.csv" locally). The dataset includes the following fitness/health metrics for 2000 individuals:
- Age
- Height (cm)
- Weight (kg)
- Heart Rate (bpm)
- Blood Pressure
- Sleep (hours)
- Nutrition Quality
- Activity Index
- Smokes
- Gender
- Fitness Level

# Dashboard Logistics
The dashboard is constructed using dash and plotly packages, which visualizes the cleaned dataset (cleaned using numpy and pandas packages) in three different visualizations: scatterplot, heatmap, and boxplot. Fitness Level (1 = fit, 0 = not fit) is used as the target metric, as chosen by feature selection among two other descriptive "fitness/nutrition indicating variables" (Smokes, Gender). 

Scatterplot: The scatterplot maps any metric against any other metric using Fitness Level as color coding, allowing the user to visually determine any correlation between two metrics in relation to Fitness Level.

Heatmap: The heatmap calculates the correlations between all metrics (and themselves as well, which naturally results in 1) and color codes them based on how close they are to perfectly positively or negatively correlated. A correlation of 0 would be white, while moving closer to 1 would result in an increasingly darker blue, and moving closer to -1 would result in an increasingly darker red. The heatmap allows the user to visually catch the strongest correlations between metrics. 

Boxplot: The boxplot visualizes the metrics that are most correlated with the target metric, Fitness Level, and maps the descriptive statistics of these metrics. 

# Model Training
The dashboard also explores what models can be used to best train the dataset, by comparing the mean absolute errors of the models against that of the baseline model. The three models used are Linear Regression, Random Forest, and Support Vector Regression, performed using sklearn packages. The user is able to toggle between the different models, located at the bottom of the dashboard, to see what model can best be used for machine learning implementations of the dataset.
