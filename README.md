# How does Generative AI usage, together with students' study habits and learning behaviours, influence their academic performance, and can we predict their post-semester GPA?

<img width="800" height="428" alt="images" src="https://github.com/user-attachments/assets/ddfed5cb-85a4-4d1a-8333-79b875ae3c5c" />


## **Background**

The growing adoption of Generative AI tools such as ChatGPT, Microsoft Copilot and Google Gemini is transforming how students learn, study and complete academic tasks. While these tools offer opportunities to improve learning efficiency, academic performance and productivity, concerns remain about their potential effects on students' independent learning, critical thinking, skill retention and psychological well-being.

This project explores the impact of AI adoption on students in higher education by analysing data across multiple dimensions, including AI usage patterns, academic performance, study behaviour, AI dependency, skill retention and student well-being. Through data analytics and machine learning, the project aims to provide a better understanding of how students interact with AI and the potential benefits and challenges associated with its growing use in education.

## **Objectives**
1. Formulate six business questions to investigate the impact of Generative AI on students' academic performance, skill retention, AI usage patterns and psychological well-being.

2. Develop a Google Looker Studio dashboard to visualise key findings, identify trends and explore relationships between AI usage and student outcomes.

3. Apply multiple linear regression to predict students' post-semester GPA using relevant features such as AI usage hours, traditional study habits, academic background and other student characteristics.

4. Interpret the analytical and predictive results to better understand the potential benefits and challenges of Generative AI adoption in higher education.

## Data Cleansing
Data cleansing was performed using Claude AI based on a predefined prompt to inspect all rows and features, identify missing values, duplicates, inconsistent formats, incorrect data types and invalid entries. Appropriate cleaning methods were applied, and the cleaned dataset was exported as ai_student_impact_cleaned.csv.

**Predefined Prompt:**

```
You are a professional data analyst. Carefully inspect the entire dataset and clean **every column and every row** based on its data type, meaning, and context. Identify and handle missing values, duplicate records, incorrect data types, inconsistent formats, spelling errors, extra spaces, invalid values, and unusual outliers. Apply suitable cleaning methods to each feature without removing valid information or making unnecessary assumptions. Ensure all columns have consistent formats and appropriate data types. After cleaning, verify that the dataset is complete, consistent, and ready for analysis. Finally, export the cleaned dataset into a new CSV file named **ai_student_impact_cleaned.csv**, keeping the original dataset unchanged. Provide a brief summary of the cleaning steps performed.
```

**Claude Output Screenshots:**
<img width="1917" height="907" alt="Screenshot 2026-11-08 094530" src="https://github.com/user-attachments/assets/dfc960ec-8df9-4df3-93eb-abceb3a47091" />

<img width="1917" height="962" alt="Screenshot 2026-11-08 094702" src="https://github.com/user-attachments/assets/352c782f-f6cb-4f43-8710-09420c8343a0" />

<img width="1917" height="962" alt="Screenshot 2026-11-08 094702" src="https://github.com/user-attachments/assets/a2934c29-41ae-41cc-9ad7-099793576eb7" />


## **Business Questions:**
The following eight business questions were developed to explore the impact of Generative AI on students, focusing on academic performance, AI usage patterns, study behaviour, skill retention and psychological well-being. These questions guide the data analysis and dashboard development to uncover meaningful insights and trends.

## **A. Generative AI usage and academic performance**

## 1. Does using Generative AI more frequently relate to better or poorer academic performance?

<img width="989" height="495" alt="BQ1" src="https://github.com/user-attachments/assets/b6240f68-6b3f-4c11-b5d1-03c562739f05" />

**Insights:**
- Students spending 40 weekly hours on GenAI achieve GPAs spanning the full 1.0 to 4.0 range, showing no major difference compared to students with low usage hours.
- For the business, this means product development should focus on guiding effective AI interaction rather than limiting student usage time.


## 2. Which academic majors have the highest Generative AI usage, and how does their GPA compare?

<img width="989" height="495" alt="BQ2a" src="https://github.com/user-attachments/assets/7685e935-e359-4c20-8eba-cbf3c7a0a62f" />

**Insights:**
- STEM and Medical majors lead slightly with an average GPA of ~3.35, while Business scores lowest at ~3.32, creating a minimal variance of only ~0.03 points across all five categories.
- For the business, this uniform baseline performance across disciplines indicates that academic major is not a key driver of GPA differences, so educational products or interventions can be broadly standardized across fields rather than customized by major.


<img width="989" height="495" alt="BQ2b" src="https://github.com/user-attachments/assets/67be24be-9ec7-40ff-a95d-0696d0aef983" />

**Insights:**
- STEM majors record the highest average usage at ~10.5 hours per week, which is significantly higher than Business (~8.25 hours), Medical (~7.5 hours), Arts (~7.25 hours), and Humanities (~6.75 hours).
- For the business, this ~3.75-hour gap between STEM and Humanities highlights higher product adoption in technical disciplines, indicating marketing and product expansion should focus on increasing engagement within non-STEM majors.


## 3. Do students who use Generative AI for different purposes achieve different academic results?

<img width="984" height="494" alt="BQ3" src="https://github.com/user-attachments/assets/35ab8dd9-c4ec-4dfd-a439-f59a4baa37f3" />

**Insights:**
- Debugging/Troubleshooting yields the highest median GPA (~3.5), whereas Direct Answer Generation results in the lowest median GPA (~3.35), showing a minimal gap of about 0.15 GPA points across primary use cases.
- For the business, this slight advantage for problem-solving use cases indicates product feature development should prioritize interactive problem-solving tools over direct content generation.

## 4. Does using a wider variety of AI tools relate to higher post-semester GPA?

<img width="989" height="495" alt="BQ4" src="https://github.com/user-attachments/assets/d71461e8-dc0c-409b-b438-28f0c0d8c3a3" />

**Insights:**
- Students using 5 distinct AI tools average a 3.35 GPA compared to 3.33 for students using only 1 or 2 tools, demonstrating a negligible difference of just ~0.02 GPA points across all tool counts.
- For the business, this flat distribution means bundling multiple niche AI features does not drive measurable academic improvement, so product strategies should focus on enhancing core platform quality rather than tool diversity.

## **B. AI Skills and Learning Effectiveness**

## 5. Do students with better prompt engineering skills achieve higher academic performance?

<img width="989" height="495" alt="BQ5" src="https://github.com/user-attachments/assets/02a585c5-a8a3-46ef-9892-c6f7f9291aac" />

**Insights:**
- Advanced prompt engineers achieve a slightly higher median GPA (~3.45) compared to both Beginners (~3.40) and Intermediates (~3.40), representing a minimal variance of only ~0.05 GPA points.
- For the business, this uniform outcome suggests that specialized prompt engineering training yields minimal direct academic gains, meaning educational AI platforms should focus on integrated core learning support rather than standalone prompting tutorials.

## 6. Do students with better skill retention achieve higher post-semester GPA?

<img width="989" height="495" alt="BQ6" src="https://github.com/user-attachments/assets/c171eacd-0748-474b-923f-f87ae64f06ca" />

**Insights:**
- High performers with 4.0 GPAs spans across retention scores from 40 to 100, while low GPAs below 2.0 become far less frequent as retention scores rise above 60.
- For the business, this positive relationship indicates that product features designed to improve knowledge retention directly support academic success, justifying investment in retention-boosting learning modules.

## 7. Does depending too much on Generative AI relate to poorer academic performance?

<img width="989" height="495" alt="BQ7" src="https://github.com/user-attachments/assets/db731495-06f7-44f7-88d5-8e5bba42afe3" />

**Insights:**
- High AI-dependent students average a ~3.38 GPA compared to ~3.35 for Low AI-dependent students, showing an insignificant gap of only ~0.03 GPA points across dependency levels.
- For the business, this uniform performance indicates that high AI reliance does not harm student grades, allowing products to focus on engagement and learning quality without risk of hurting academic outcomes.

## 8. Do students with different levels of AI dependency have different skill retention scores?

<img width="989" height="495" alt="output" src="https://github.com/user-attachments/assets/904dc7de-7723-4eaa-a59a-07b22c7e29b3" />

**Insights:**
- Median skill retention scores stay steady at ~75 to ~76 for dependency levels 1 through 6, but drop sharply to ~65 at level 10, creating an 11-point decline.
- For the business, this drop shows that over-reliance on AI harms long-term learning, meaning the platform should add active recall prompts or guardrails when user dependency rises above level 6.


## Google Data Studio (Dashboard)

Here is the link to the Impact of AI on Students dashboard, developed based on the six selected business questions. It provides interactive visualisations and insights into AI usage patterns, academic performance, skill retention and student well-being.

https://datastudio.google.com/reporting/4a84b489-215e-4090-ad84-ac3c7f4455d3

<img width="1917" height="830" alt="Screenshot 2026-11-09 170052" src="https://github.com/user-attachments/assets/e1f58102-5dad-47c7-800c-2dfc158fceab" />



## Predictive Modelling (Regression) 
Predictive modelling was conducted using multiple regression-based machine learning models to examine the relationships between students' Generative AI usage patterns, study habits, and other student-related factors and their post-semester GPA. The objective was to determine whether these factors could be used to predict students' academic performance after adopting Generative AI tools.

Post-Semester GPA was selected as the prediction target because it provides a measurable indicator of students' academic performance following the adoption of Generative AI. It also addresses the eight business questions by examining how AI usage patterns, study habits, academic background, prompt engineering skills, AI dependency, skill retention, and student well-being relate to academic outcomes. By predicting post-semester GPA using these relevant factors, the project extends the dashboard analysis beyond identifying trends and relationships to evaluating the predictive value of these factors.

The models were evaluated using Mean Absolute Error (MAE), Mean Squared Error (MSE), Root Mean Squared Error (RMSE), and R-squared (R²) on both the training and testing datasets.

| Model | Train MAE | Train MSE | Train RMSE | Train R2 |
|:---|:---|:---|:---|:---|
|DTR|0.0000|0.0000|0.0000|1.0000|
|RFR|0.0452|0.00341|0.0584|0.9862|
|GBR|0.1141|0.0210|0.1450|0.9148|
|ETR|0.0000|0.0000|0.0000|1.0000|


| Model | Test MAE | Test MSE | Test RMSE | Test R2 |
|:---|:---|:---|:---|:---|
|DTR|0.1716|0.0495|0.2225|0.7948|
|RFR|0.1207|0.0237|0.1541|0.9017|
|GBR|0.1144|0.0210|0.1449|0.9130|
|ETR|0.1203|0.0234|0.1531|0.9029|





Gradient Boosting Regressor (GBR) was identified as the most suitable model for prediction. It achieved the lowest testing MAE (0.1144), MSE (0.0210), and RMSE (0.1449), together with the highest testing R² (0.9130). These results indicate that GBR provides the most accurate predictions among the four models and explains approximately 91.3% of the variation in post-semester GPA in the testing dataset. Its training and testing performance are also relatively consistent, suggesting better generalisation and less overfitting than the Decision Tree Regressor (DTR) and Extra Trees Regressor (ETR).



## References
https://www.kaggle.com/datasets/laveshjadon/ai-impact-on-students
