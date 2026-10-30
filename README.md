# Student Performance & Socioeconomic Analytics

## Project Overview
This project delivers an end-to-end Exploratory Data Analysis (EDA) evaluating the socioeconomic, demographic, and academic preparation factors that influence student performance. Using a dataset of 1,000 student records, the analysis identifies key achievement gaps across distinct student subgroups and establishes data-driven recommendations for educational interventions.

The project was executed in a collaborative data science bootcamp environment, focusing on structured data validation, feature engineering, and statistical visualization.

## Dataset & Feature Schema
The dataset consists of 1,000 distinct student rows across 8 base features:
* Categorical Attributes: `gender`, `race/ethnicity`, `parental level of education`, `lunch` (economic proxy), `test preparation course`
* Quantitative Metrics: `math score`, `reading score`, `writing score`

## Data Engineering & Pipeline
Prior to analysis, the data underwent a comprehensive quality assurance check inside a Jupyter Notebook environment:
* Integrity Audits: Missing value evaluation (`df.isnull().sum()`) and duplicate detection (`df.duplicated().sum()`) confirmed 100% data completeness with zero duplicate anomalies.
* Domain Validation: Boundaries were systematically checked to ensure all test scores fell within valid standard limits (0 to 100).
* Feature Engineering: Constructed an aggregate metric, `average_score`, calculating the localized mean across math, reading, and writing disciplines for each record to provide a unified benchmark.

## Key Insights & Statistical Findings

### 1. Test Preparation Impact
* Finding: Students who completed test preparation programs consistently outperformed those who did not across all three subjects.
* Strategic Action: Institutionalize test preparation frameworks, prioritizing enrollment for historically low-performing students.

### 2. Economic Disparities (Lunch Type Proxy)
* Finding: A pronounced achievement gap exists based on student lunch status. Students receiving standard lunch achieved significantly higher average scores than those on free or reduced lunch programs.
* Strategic Action: Deploy targeted academic resources, subsidies, and free after-school tutoring specifically for economically disadvantaged student populations.

### 3. Parental Educational Attainment
* Finding: Higher levels of parental education directly correlate with increased student test scores. Students whose parents hold master's or bachelor's degrees secured the highest placement on the performance spectrum.
* Strategic Action: Develop school-led mentoring programs to provide additional structural guidance to students whose families lack higher education experience.

### 4. Gender Performance Variance
* Finding: Distinct performance splits were observed between genders. Female students demonstrated higher proficiency in reading and writing, while male students performed higher in mathematics.
* Strategic Action: Target educational support by gender, offering reading and writing reinforcement modules for male students and math confidence initiatives for female students.

## Technology Stack & Libraries
* Data Manipulation: Python, NumPy, Pandas
* Data Visualization: Matplotlib, Seaborn, Plotly, Missingno
