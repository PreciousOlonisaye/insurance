
# Healthcare Insurance Customer Data Analysis

## Problem Statement
The goal of this dashboard is to gain insights into the factors influencing health insurance charges. In order to identify patterns, correlations, and trends that can help in understanding the key drivers of health insurance costs.

### Introduction
In an era where healthcare costs continue to be a significant concern, insurance helps to reduce the cost of healthcare services, understanding the underlying factors that contribute to insurance charges is crucial for informed decision-making and resource allocation. 

### Dataset Description
age: age of the primary beneficiary
Sex: insurance contractor gender, female, male
age: Body mass index, providing an understanding of body, weights that are relatively high or low relative to height, objective index of body weight (kg / m ^ 2) using the ratio of height to weight, ideally 18.5 to 24.9
Children: Number of children covered by health insurance / Number of dependents
Smoker: Smoking
Region: the region the customer is located in, the categories include the northeast, southeast, southwest and northwest.
Charges: Individual medical costs billed by health insurance

### Tools
Microsoft Excel: Data Exploration, Data Cleaning and Preparation	
Microsoft Word: Documentation.
Microsoft Power BI: Data Visualization and dashboard.


### Steps followed
- Step 1 : Load data in excel and check for missing values or null values. It was observed that none of the columns contained errors and empty values.
- Step 2 : Load data into Power BI Desktop, dataset is a csv file.
Converted data in the smoker column from "yes and no" to "smoker and non-smoker"
- Step 3 : The summary statistics of the age column was caculated using the following steps:
1. New measure was created to calculate mean age:
Mean(age) = AVERAGE(insurance[age])

A visual card was used to represent the mean age. 
![Mean(Age)](https://github.com/PreciousOlonisaye/Precious_portfolio/assets/101580779/44632e51-a2f0-4bba-ba6d-f9e3f8e778d9)

2. New measure was created to calculate the median age:
Median(age) = MEDIAN(insurance[age] 

A visual card was used to represent the median age
![Median(Age)](https://github.com/PreciousOlonisaye/Precious_portfolio/assets/101580779/111e60ca-b7a7-4ddf-b6c5-7dbd98f53c49)

3. The most frequently occuring age in the dataset was calculated by creating a new measure:
Mode (age) = MINX(TOPN(1, ADDCOLUMNS(VALUES(insurance[age]), "percent", CALCULATE(COUNT(insurance[age]))),[percent],DESC), insurance[age])

This was represented using a visual card
![Mode(Age)](https://github.com/PreciousOlonisaye/Precious_portfolio/assets/101580779/24ab5a18-d061-454e-be45-4e2183169865)

4. The range of the age column was calculated using a new measure:
RANGE(age) = MAX(insurance[age]) - MIN(insurance[age])

This was represented using a visual card
![Range(Age)](https://github.com/PreciousOlonisaye/Precious_portfolio/assets/101580779/b038508a-ae49-4cd8-8b10-0dd41d97411a)
5. The first quartile, second quartile and third quartile of the age column was calculated using the following measures:
Q1(age) = PERCENTILE.EXC(insurance[age], 0.25
Q2(age) = PERCENTILE.EXC(insurance[age], 0.5)
Q3(age) = PERCENTILE.EXC(insurance[age], 0.75)

This were represented using a visual card
![Q2(Age)](https://github.com/PreciousOlonisaye/Precious_portfolio/assets/101580779/4847671d-9bdc-4de8-b24c-4cecd587477a)
![Q3(AGE)](https://github.com/PreciousOlonisaye/Precious_portfolio/assets/101580779/3e5aa320-9937-474e-bb6f-8f67666de269)

6. The standard deviation of the age column was calculated by creating new measures:
STANDARD DEVIATION(age) = STDEV.P(insurance[age]) 

7. The variance of the age column was calculated:
VARIANCE(age) = VAR.P(insurance[age])

This was represented using a visual card
![Variance(Age)](https://github.com/PreciousOlonisaye/Precious_portfolio/assets/101580779/04c15dad-cbf8-46ad-b867-54c6b5bf8173)

- Step 4 : The summary statistics of the bmi column was caculated using the following steps:
1. New measure was created to calculate mean bmi:
Mean(bmi) = AVERAGE(insurance[bmi]) 

This was represented using a visual card
![Mean(BMI)](https://github.com/PreciousOlonisaye/Precious_portfolio/assets/101580779/9fb3467e-933b-4744-be6b-327c1de4ff77)

2. New measure was created to calculate the median bmi:
Median(bmi) = MEDIAN(insurance[bmi] 

This was represented using a visual card
![Median(BMI)](https://github.com/PreciousOlonisaye/Precious_portfolio/assets/101580779/e3e8ba2a-0089-4ba7-8e70-2aacb3dbb542)
3. The most frequently occuring bmi in the dataset was calculated by creating a new measure:
Mode (bmi) = MINX(TOPN(1, ADDCOLUMNS(VALUES(insurance[bmi]), "percent", CALCULATE(COUNT(insurance[bmi]))),[percent],DESC), insurance[bmi])

This was represented using a visual card
![Mode(BMI)](https://github.com/PreciousOlonisaye/Precious_portfolio/assets/101580779/c84a0302-1120-4bb9-aefa-d2ca94484200)
4. The range of the bmi column was calculated using a new measure:
RANGE(bmi) = MAX(insurance[bmi]) - MIN(insurance[bmi])

This was represented using a visual card
![RANGE(BMI)](https://github.com/PreciousOlonisaye/Precious_portfolio/assets/101580779/cdf94b3c-04be-4682-872a-5f3b8e6970cc)

5. The first quartile, second quartile and third quartile of the bmi column was calculated using the following measures:
Q1(bmi) = PERCENTILE.EXC(insurance[bmi], 0.25
Q2(bmi) = PERCENTILE.EXC(insurance[bmi], 0.5)
Q3(bmi) = PERCENTILE.EXC(insurance[bmi], 0.75)

This were represented using visual cards
![Q2(BMI)](https://github.com/PreciousOlonisaye/Precious_portfolio/assets/101580779/d1ce728f-0883-4af2-871f-6782b9a51ea9)


6. The standard deviation of the bmi column was calculated by creating new measures:
STANDARD DEVIATION(bmi) = STDEV.P(insurance[bmi]) 

This was represented using a visual card
![STANDARD DEVIATION(BMI)](https://github.com/PreciousOlonisaye/Precious_portfolio/assets/101580779/02d3af15-dc39-42d7-a517-7103f79a79b8)
7. The variance of the bmi column was calculated:
VARIANCE(bmi) = VAR.P(insurance[bmi])
![VARIANCE(BMI)](https://github.com/PreciousOlonisaye/Precious_portfolio/assets/101580779/8bc18b4f-9b0b-4328-a720-e349f3eb60d6)

- Step 5: The summary statistics of the charges column was caculated using the following steps:
1. New measure was created to calculate mean charges:
Mean(charges) = AVERAGE(insurance[charges]) 

This was represented using a visual card
![Mean(Charges)](https://github.com/PreciousOlonisaye/Precious_portfolio/assets/101580779/a3aafa1b-e27e-44e8-b4fa-ca5da9b2a877)

2. New measure was created to calculate the median charges:
Median(charges) = MEDIAN(insurance[charges])

This was represented using a visual card
![Median(Charges)](https://github.com/PreciousOlonisaye/Precious_portfolio/assets/101580779/0561acdc-7ca6-431d-a1ef-891eb02ae2f9)

3. The most frequently occuring charges in the dataset was calculated by creating a new measure:
Mode (charges) = MINX(TOPN(1, ADDCOLUMNS(VALUES(insurance[charges]), "percent", CALCULATE(COUNT(insurance[charges]))),[percent],DESC), insurance[charges])

This was represented using a visual card
![Mode(Charges)](https://github.com/PreciousOlonisaye/Precious_portfolio/assets/101580779/b628af64-56eb-4368-9694-9a1c929a0609)
4. The range of the charges column was calculated using a new measure:
RANGE(charges) = MAX(insurance[charges]) - MIN(insurance[charges])

This was represented using a visual card
![Range(charges)](https://github.com/PreciousOlonisaye/Precious_portfolio/assets/101580779/f7b99f33-aa85-4364-9605-b71c7db90dc8)

5. The first quartile, second quartile and third quartile of the charges column was calculated using the following measures:
Q1(charges) = PERCENTILE.EXC(insurance[charges], 0.25
Q2(charges) = PERCENTILE.EXC(insurance[charges], 0.5)
Q3(charges) = PERCENTILE.EXC(insurance[charges], 0.75)

This were represented using visual cards
![Q1(Charges)](https://github.com/PreciousOlonisaye/Precious_portfolio/assets/101580779/4de4c0d8-0ac3-4803-9cd0-6e5530a5a9d1)
![Q2(charges)](https://github.com/PreciousOlonisaye/Precious_portfolio/assets/101580779/cb1848a8-cbc2-4f72-9cc3-2452d231c03e)
![Q3(charges)](https://github.com/PreciousOlonisaye/Precious_portfolio/assets/101580779/4bf67023-f2b1-47df-8604-d50605741383)

6. The standard deviation of the charges column was calculated by creating new measures:
STANDARD DEVIATION(charges) = STDEV.P(insurance[charges]) 

This was represented using a visual card
![Standard deviation(Charges)](https://github.com/PreciousOlonisaye/Precious_portfolio/assets/101580779/8fd1548e-1ebf-42ee-ba16-cbf22a15c1d0)

7. The variance of the charges column was calculated:
VARIANCE(charges) = VAR.P(insurance[charges])

This was represented using a visual card
![Variance(charges)](https://github.com/PreciousOlonisaye/Precious_portfolio/assets/101580779/4dcae196-2204-4e9a-911f-790774c0a642)

- Step 6 : The summary statistics of the children column was caculated using the following steps:
1. New measure was created to calculate mean children:
Mean(children) = AVERAGE(insurance[children]) 

This was represented using a visual card
![Mean(children)](https://github.com/PreciousOlonisaye/Precious_portfolio/assets/101580779/78f92958-d589-4fdd-9c4b-8654e452d139)

2. New measure was created to calculate the median children:
Median(children) = MEDIAN(insurance[children])

This was represented using a visual card
![Median(children)](https://github.com/PreciousOlonisaye/Precious_portfolio/assets/101580779/09f75965-cdb7-4c27-bd7b-2896d9f0a04d)
3. The most frequently occuring children in the dataset was calculated by creating a new measure:
Mode (children) = MINX(TOPN(1, ADDCOLUMNS(VALUES(insurance[children]), "percent", CALCULATE(COUNT(insurance[children]))),[percent],DESC), insurance[children])

This was represented using a visual card
![mode(children)](https://github.com/PreciousOlonisaye/Precious_portfolio/assets/101580779/17d04c8e-459e-4c45-af9a-9d3b8b4b6ab1)

4. The range of the children column was calculated using a new measure:
RANGE(children) = MAX(insurance[children]) - MIN(insurance[children])

This was represented using a visual card
![range(children)](https://github.com/PreciousOlonisaye/Precious_portfolio/assets/101580779/edd51df9-c43c-4145-bc94-fa7226a6cfca)
5. The first quartile, second quartile and third quartile of the children column was calculated using the following measures:
Q1(children) = PERCENTILE.EXC(insurance[children], 0.25
Q2(children) = PERCENTILE.EXC(insurance[children], 0.5)
Q3(children) = PERCENTILE.EXC(insurance[children], 0.75)

This were represented using visual cards

![q1(children)](https://github.com/PreciousOlonisaye/Precious_portfolio/assets/101580779/3e915c3b-3455-4816-8a7f-76fa16838855)
![q2(children)](https://github.com/PreciousOlonisaye/Precious_portfolio/assets/101580779/0254ea09-d0cf-4c8b-a156-aefd37a11670)
![q3(children)](https://github.com/PreciousOlonisaye/Precious_portfolio/assets/101580779/e672e3e5-7adb-41ae-bb3f-0b9868637f6d)
6. The standard deviation of the children column was calculated by creating new measures:
STANDARD DEVIATION(children) = STDEV.P(insurance[children]) 

This was represented using a visual card
![standard deviation(children)](https://github.com/PreciousOlonisaye/Precious_portfolio/assets/101580779/30777ec4-678d-4147-a052-72615f0c8a26)
7. The variance of the children column was calculated:
VARIANCE(children) = VAR.P(insurance[charges])

This was represented using a visual card
![variance(children)](https://github.com/PreciousOlonisaye/Precious_portfolio/assets/101580779/5efe51f1-6f60-41b9-87fc-8a662eedee1a)

- Step 7 :
The count of unique values in the categorical columns were taken
Sex:
COUNT(SEX) = COUNT(insurance[Sexs])

This was represented using a visual card
![COUNT(SEX)](https://github.com/PreciousOlonisaye/Precious_portfolio/assets/101580779/0757cda3-4599-4a6f-8b83-61ff686afe8a)
Smoker:
COUNT(Smoker) = COUNT(insurance[Smoker])

This was represented using a visual card
![COUNT(SMOKER)](https://github.com/PreciousOlonisaye/Precious_portfolio/assets/101580779/5b97e08d-7824-4528-b22f-827de55d2d18)

Region:
COUNT(Region) = COUNT(insurance[Region])

This was visualised using a visual card
![COUNT(REGION)](https://github.com/PreciousOlonisaye/Precious_portfolio/assets/101580779/7c5a3dde-4857-4e7f-9245-5375c11ddbe1)

- Step 8:
A new computed column was added in which customers were seperated into different age groups.
![image](https://github.com/PreciousOlonisaye/Precious_portfolio/assets/101580779/6498a747-b083-4692-97b2-64cf0cf12f73)

-  Step 9: In the report view, under the insert tab using shapes option, a rectangle was inserted and a prefered colour was chosen. Using a text box, the title of the dashboard was then added. This serves as the header of the dashboard.
- Step 10 :
In the report view, under the view tab, theme was selected
- Step 11:
Visual filters "Slicers" were added for four fields named "Sex", "Age bracket", "Smoker" and "Region".
- Step 12:
In the report view, under the insert tab, using shapes option from elements group a rounded rectangle was inserted, its colour was adjusted to white, it was then duplicated, it serves as the background for the visuals
- Step 13: The following visuals were then added
1. A Stacked bar chart average charge by age
2. Bubble chart average charge by region
3. Stacked column chart average charge by smoker status and average charge by sex
4. Area chart average insurance by number of children
5. Line chart average charge by BMI
6. Ribbon chart Average of BMI by Smoker Status and Sex

### The following is a snapshot of the dashboard
![image](https://github.com/PreciousOlonisaye/Precious_portfolio/assets/101580779/04b35fbc-b5b4-4dcc-8972-8b8ffcd2b565)

