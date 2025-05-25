**Note**
This Project is based on the Statistical Approach that we studied entirely in our Probability and Statistics course

**Problem Statement**
How can policymakers determine action steps to take to promote the health and longevity of their nation’s citizens? What factors might be at play that can affect a person’s lifespan? In this situation, we will be exploring a dataset with the life expectancy of people from various nations over time, along with various factors that may contribute to this life expectancy.

**Questions we Covered**

What particular health or socioeconomic factors contribute to a person’s average life expectancy?
Which particular models can provide the strongest prediction in answering the previous question?

**Dataset Acquisition:**
To answer the research questions above, this project requires a dataset with average life expectancy in various locations, along with health, immunization, and socioeconomic data for each of those locations. Such a dataset was acquired from Kaggle, which is an online platform for data science enthusiasts. The link to this dataset can be found here: 
📊 [Life Expectancy WHO Dataset on Kaggle](https://www.kaggle.com/datasets/lashagoch/life-expectancy-who-updated)

The dataset contains records of 179 countries between the years 2000 and 2015. Each record is of an individual year in an individual country, along with the corresponding life expectancy, health, immunisation, and socioeconomic data for that year in that country. The data was collected by the World Health Organisation and the World Bank, and compiled and cleaned by the publisher of this dataset.
**Key Variable:**
1. Polio: float value of the percentage of 1-year-old children immunised from Polio
2. GDP_per_capita: float value of a nation’s gross domestic product per capita
3. Adult_mortality: float value of the number of adult deaths between ages 15 and 60 per 1000 people
4. Schooling: float value of the average number of years that people aged 25 years and older spent in formal education.\
**Target Variable**
Life_expectancy: float value of gender-agnostic average life expectancy in a given nation in a given year; this is the target variable

**Data Preparation**
In our Data Preparation we explored the data visualisation and outlier part concerning our key variable and the Target available

**Data Modelling**
1. Simple Linear Regression
2 .Multiple Linear Regression
3. ElasticNet Regression 
4. Chi-Square Test

**Model Deployment**
The model deployment was initially conducted using multiple linear regression. One of our key variables was alcohol consumption, which seemed to exhibit a confounding effect. Specifically, we observed that increasing alcohol consumption correlated with higher average schooling, leading to predictions of life expectancy exceeding 70 years. We found this correlation to be irrelevant to our study.

To improve our model, we switched to elastic net regression, which helped us gain a clearer perspective on the key variables. As a result, we decided to exclude alcohol consumption from our key variables. We then deployed the adjusted model using elastic net through Hugging Face to enhance its performance in real-time, making it more accessible to users.

🔗 [Try the Life Expectancy Predictor](https://huggingface.co/spaces/1907adi/Life_Expectancy_Predictor)
