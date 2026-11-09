# Impact of AI on Students

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

### 1. Does using AI more frequently affect students' academic performance?

<img width="996" height="494" alt="Q1" src="https://github.com/user-attachments/assets/e3e850d4-947a-4195-868a-06a381f55794" />

**Insights:**
- There is virtually no linear relationship between the number of weekly GenAI hours (ranging from 0 to 40 hours) and a student's post-semester GPA (ranging from 1.0 to 4.0), showing that higher tool usage does not inherently harm or help academic performance.

- EdTech and AI platforms should pivot from marketing tools based solely on time-saving or grade-boosting claims; instead, they should focus on providing quality guidance and qualitative learning outcomes to drive true value for educational institutions.


### 2. Does AI usage reduce students traditional study time?

<img width="993" height="494" alt="Q2" src="https://github.com/user-attachments/assets/be1db70b-0db3-412e-af4a-69c5db99fc71" />

**Insights:**
- There is a slight negative relationship between weekly GenAI usage (0 to 40 hours) and traditional study hours (0 to 35 hours), showing that as students rely more on AI, their dedicated non-AI study time slightly decreases.
- EdTech companies can position AI products as efficiency tools that reduce manual study time, but educators must ensure AI is used to enhance study habits rather than completely replace core learning efforts.

### 3. Which academic majors uses AI the most?

<img width="1189" height="495" alt="Q3" src="https://github.com/user-attachments/assets/3d34371d-91a1-47c5-8c7c-577bd14ce414" />

**Insights:**
- STEM majors lead GenAI adoption with highest weekly usage at ~10.5 hours, followed by Business (~8.3 hrs), Medical (~7.5 hrs), Arts (~7.3 hrs), and Humanities trailing at ~6.8 hours.
- EdTech developers should prioritize specialized coding, technical, and analytical AI features for high-frequency STEM users while creating tailored marketing to encourage adoption among lower-use majors like Humanities.


### 4. Does AI dependency affect students' skill retention?

<img width="1189" height="494" alt="Q4" src="https://github.com/user-attachments/assets/9f43eaf8-c5be-4e0b-a75d-afec05f6d91f" />

**Insights:**
- High AI dependency reduces the median skill retention score to ~71, compared to ~76 for both Low and Moderate AI dependency groups.
- EdTech platforms and training providers should design interactive learning features that limit over-reliance on AI, ensuring users retain core skills alongside automated assistance.


### 5. Which students have the highest burnout risk?

<img width="1189" height="495" alt="Q5" src="https://github.com/user-attachments/assets/7ba17a0d-e098-471d-b93e-71877b590938" />

**Insights:**
- Students with High AI Usage face the highest High Burnout Risk at ~56%, which is over 2.5 times higher than Medium Usage (~21%) and nearly 5.6 times higher than Low Usage (~10%).
- EdTech platforms and universities must incorporate wellness features, workload management, and healthy usage guidelines into AI tools to prevent student over-reliance and burnout.


### 6. Does prompt engineering skill influence students' academic performance?

<img width="1189" height="495" alt="Q6" src="https://github.com/user-attachments/assets/c21f44a4-7c45-4f0b-90b3-3ffbfe5fa684" />

**Insights:**
- Median post-semester GPA remains nearly identical across all prompt engineering skill levels, peaking slightly at ~3.48 for Advanced users compared to ~3.40 for both Beginner and Intermediate levels.
- EdTech platforms should avoid marketing prompt engineering skills as a direct driver of higher academic grades, and instead focus on positioning these skills around workflow efficiency, creativity, and time management.

### 7. What are the most common purposes for which students use Generative AI?

<img width="871" height="475" alt="Q7" src="https://github.com/user-attachments/assets/5a6bb6f8-0c02-4034-a45d-75737530bfb6" />

**Insights:**
- Debugging/Troubleshooting (24.6%) and Copywriting/Drafting (24.0%) are the top student use cases, together making up nearly half (48.6%) of AI activity, whereas Direct Answer Generation accounts for the smallest share at 12.7%.
- EdTech developers should focus product optimization and marketing on technical troubleshooting, writing assistance, and ideation features (21.4%), which represent the vast majority of organic student demand.


### 8. What is the distribution of student's post-semester GPA?

<img width="1189" height="495" alt="Q8" src="https://github.com/user-attachments/assets/a036b108-0c88-40d3-8926-ac2d71a77691" />

**Insights:**
- The GPA distribution shows a dramatic spike at 4.0, where nearly 5,800 students reach the maximum score compared to a steady spread of around 1,000 to 1,500 students per bin across the 3.0–3.9 range.
- Educational analytics providers and institutions should account for ceiling effects in GPA metrics, as standard GPA scores alone may obscure finer differences in student performance and learning growth.

## Google Data Studio (Dashboard)

Here is the link to the Impact of AI on Students dashboard, developed based on the six selected business questions. It provides interactive visualisations and insights into AI usage patterns, academic performance, skill retention and student well-being.

https://datastudio.google.com/reporting/4a84b489-215e-4090-ad84-ac3c7f4455d3


## Predictive Modelling (Regression) 
Predictive modelling was implemented using multiple linear regression to examine how AI usage patterns, study habits and other student-related factors are associated with post-semester GPA. The objective is to understand how these factors contribute to predicting students' academic performance after adopting Generative AI tools.

**Post-Semester GPA was selected as the prediction target because it provides a measurable indicator of students' academic performance after using Generative AI.** It directly connects to the eight business questions by allowing us to examine how AI usage patterns, study habits, academic background, prompt engineering skills, AI dependency, skill retention and student well-being relate to academic outcomes. Using multiple linear regression, the project aims to predict students' post-semester GPA based on these relevant features, extending the dashboard analysis from identifying trends and relationships to predictive modelling.

TBC



## References
https://www.kaggle.com/datasets/laveshjadon/ai-impact-on-students
