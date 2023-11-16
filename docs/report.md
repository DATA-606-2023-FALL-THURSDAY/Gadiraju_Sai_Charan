                                                              
# Title and Author

- **Project Title**: Capstone Project on H1 VISA Status Prediction using Machine Learning Models 
- **Prepared for UMBC Data Science Master Degree Capstone by**: Dr. Chaojie (Jay) Wang
- **Author**: Gadiraju Sai Charan
- **Link to the author's GitHub profile**: [GitHub Profile](https://github.com/Saicharan0297)
- **Link to the author's LinkedIn profile**: [LinkedIn Profile](https://www.linkedin.com/in/sai-charan-gadiraju/)
- **Link to PowerPoint presentation file**: Will update later 
- **Link to Youtube Video**: Will Update later

# Background

For this project, I will analyze the PERM (Program Electronic Review Management) disclosure files provided by the U.S. Department of Labor's Employment and Training Administration (ETA). These disclosure files contain valuable information about foreign labor certification programs in the United States.

## What is H-1B VISA?
- H-1B visas are a category of employment-based, non-immigrant visas for temporary foreign workers in the United States. 
- For a foreign national to apply for H1-B visa, a US employer must offer them a job and submit a petition for a H-1B visa to the US immigration department. 
- This is also the most common visa status applied for and held by international students once they complete college or higher education and begin working in a full-time position.
- The duration of stay is three years, extendable to six years, after which the visa holder may need to reapply.

### Data Source
- **Data Provider**: Kaggle, and U.S. Department of Labor, ETA
- **Dataset Link**: [PERM Program - Fiscal Year 2022, 2021, 2020, 2019, 2018, 2017 Disclosure Files]([(https://www.kaggle.com/datasets/jishnukoliyadan/lca-programs-h1b-h1b1-e3-visa-petitions)])
- **Data Description**: The dataset consists of disclosure files for the PERM program, a labor certification program for employers seeking to hire foreign workers for permanent employment in the United States.

# Data

- The dataset consists of last four years information (2017-2022)
- Source: [Dataset Source]([https://www.dol.gov/agencies/eta/foreign-labor/performance](https://www.kaggle.com/datasets/jishnukoliyadan/lca-programs-h1b-h1b1-e3-visa-petitions))  Kaggle,LCA-programs-h1b-h1b1-e3-visa-petitions, U.S. Department of Labor, ETA
- Data Size: 424.4+ MB
- Data Shape (Number of Rows and Columns): Number of rows: 3973349, Number of columns: 13
- Every row describes applicant information.
- Columns:
  - Visa_Class -  It typically refers to the category or type of visa an individual is applying for, such as H-1B, H-1B1, E-3, etc.
  - EMPLOYER_NAME - Legal business name of the employer requesting permanent labor certification.
  - SOC_Title - This refers to the Standard Occupational Classification (SOC) title, which is a standardized system used to classify and categorize occupations in the United States.
  - Job_Title - It refers to the specific designation or title associated with a particular employment position held by an individual, often indicating the nature or type of work they perform within an organization.
  - Full_Time_Position - It typically denotes whether a job or position is designated as a full-time role, indicating that the employee is expected to work a standard number of hours per week, usually 35-40 hours, depending on the organization's policy.
  - Worksite - "Worksite" refers to the physical location or geographical site where employees perform their job duties. In the context of visa applications, it could represent the specific location or address of the employer where the work is primarily carried out.
  - Prevailing_Wage - "Prevailing_Wage" is the average wage paid to similarly employed workers in a specific occupation in a particular geographic area, as determined by the U.S. Department of Labor. It serves as a baseline to ensure that foreign workers are not being paid less than the average for their job and locations.
  - Unit_Of_Pay - It refers to the measurement or basis used to specify the compensation for a particular job, such as hourly, weekly, monthly, or annually. It indicates how the salary or wage for a position is calculated and presented.
  - Employer_Location - It refers to the geographic location or address where the employer's main office or headquarters is situated.
  - Employer_Country - It refers to the country where the employer is based or headquartered. It signifies the home country of the organization submitting the visa application.
  - CASE_STATUS - Status associated with the last significant event or decision. Valid values include “Certified”, “Certified-Expired”, “Denied”, and “Withdrawn”. 
  -  Year - It indicates the year of applications.

### Target Variable- CASE_STATUS - Valid values include “Certified”, “Certified-Expired”, “Denied”, and “Withdrawn”

## Project Objective

The primary objective of this data science project is to explore, analyze, and gain insights from the PERM program disclosure data for the fiscal years 2017-2022. I aim to answer various research questions, uncover trends, and provide valuable information.

# Research Questions

"What are the trends and patterns in H1B visa applications in the United States from 2017 to 2022, focusing on factors such as the overall growth in the number of applications, the top companies providing H1B sponsorships, key roles in demand, salary distributions for these roles, characteristics of data-related roles, acceptance and rejection rates, and geographical concentrations of applications across different parts of the United States?"

"Finding the accuracy using Logistic Regression, Random Forest, and Decision Tree Classifiers."

# EDA  

**1. Number of petitions per Case Status**

 <img width="700" height="500" alt="image" src="https://github.com/DATA-606-2023-FALL-THURSDAY/Gadiraju_Sai_Charan/blob/main/Images/1.JPG">

 **Observation:**
 The above bar chart shows the case status vs number of petitions for 2017-2022.
- There are four values for case status column.
- There are total of 3611457 petitions for 'CERTIFIED', 227347 for 'CERTIFIED-WITHDRAWN', 100097 for 'WITHDRAWN', and 34448 for 'DENIED'.

**2. Total number of Applications per year**

 <img width="700" height="500" alt="image" src="https://github.com/DATA-606-2023-FALL-THURSDAY/Gadiraju_Sai_Charan/blob/main/Images/2.JPG">

  **Observation:**
- The year 2021 has the highest number of applications '826305'.
- Almost for the year 2022, 2019, 2018, and 2017 the number of applications are same.
- The least is in the year 2020, maybe there can be few reasons as one of them is COVID pandemic.

 **3. The top 15 employers filing the H1-B visa petitions**

 <img width="700" height="500" alt="image" src="https://github.com/DATA-606-2023-FALL-THURSDAY/Gadiraju_Sai_Charan/blob/main/Images/3.JPG">

 **Observation:**
- Cognizant, Infosys Ltd, and Tata Consultancy are among the Top 3 employers filing for H1B.
- Also the Top Giant, Google, Amazon, and microsoft filed more than the average petitions.

 **4. The top 15 SOC names for which H1-B visas are raised**

 <img width="700" height="500" alt="image" src="https://github.com/DATA-606-2023-FALL-THURSDAY/Gadiraju_Sai_Charan/blob/main/Images/4.JPG">

 **Observation:**
- Software Developers are among the Top in demand positions. There is a huge difference between Top 2 demand positions.
- We can see the trend is towards the information technology related positions that have been filed for H1B visas during 2017-2022.

 **5. Acceptance rate of the H1-B Visa petitions through different years**

 <img width="700" height="500" alt="image" src="https://github.com/DATA-606-2023-FALL-THURSDAY/Gadiraju_Sai_Charan/blob/main/Images/5.JPG">

 <img width="700" height="500" alt="image" src="https://github.com/DATA-606-2023-FALL-THURSDAY/Gadiraju_Sai_Charan/blob/main/Images/5.1.JPG">

 **Observation:**
- The number of petitions almost increasing every year, rather than 2020 as it is an exception year due to COVID pandemic.
- Even in 2020, almost 600000 petitions were applied.
- The highest was in 2021, with almost 800000 petitions.
- The acceptance ratio is more than 80% in each year.

 **6. Salaries trend per year**

 <img width="700" height="500" alt="image" src="https://github.com/DATA-606-2023-FALL-THURSDAY/Gadiraju_Sai_Charan/blob/main/Images/6.JPG">

 **Observation:**
- The median wage is increasing every year. 
- There has been atleast 10% increase in wages except in 2022.
- The year 2020 has seen a decrease in the median wage.

 **7. Top Job Titles**

 <img width="700" height="500" alt="image" src="https://github.com/DATA-606-2023-FALL-THURSDAY/Gadiraju_Sai_Charan/blob/main/Images/7.JPG">

**Observation:**
- The Job title, Software engineer and software developer are the Top 2 during 2017-2022.
- As we can see the Top 10 Job Title are from the Information Technology related fields.

 **8. Number of applications for the Full Time Positions**

 <img width="400" height="400" alt="image" src="https://github.com/DATA-606-2023-FALL-THURSDAY/Gadiraju_Sai_Charan/blob/main/Images/8.JPG">

 **Observation:**
- We see almost 90% of the Job applied are 'Full Time Positions'.

# Techniques and Models

I will be using Machine Learning Techniques to find out the accuracy using three classifiers:

**1. Random Forest**
- **Accuracy:** 0.9570
- **Precision Score:** 0.9656
- **Recall Score:** 0.9852
- **F1 Score:** 0.9757

**2. Decision Tree**
- **Accuracy:** 0.9566
- **Precision Score:** 0.9664
- **Recall Score:** 0.9852
- **F1 Score:** 0.9757
  
**3. Logistic Regression**
- **Accuracy:** 0.9604
- **Precision Score:** 0.9664
- **Recall Score:** 0.9852
- **F1 Score:** 0.9757

# Conclusion

### Petition Distribution (Case Status):

- **Certified:** 3,611,457 petitions
- **Certified-Withdrawn:** 227,347 petitions
- **Withdrawn:** 100,097 petitions
- **Denied:** 34,448 petitions

### Application Trends:

- Peak in 2021 with 826,305 applications
- Consistent numbers for 2022, 2019, 2018, and 2017
- Decrease in 2020, attributed to the COVID-19 pandemic

### Top Employers:

- Cognizant, Infosys Ltd, Tata Consultancy lead in filings
- Tech giants (Google, Amazon, Microsoft) exceed average petitions

### Occupation Trends:

- Software Developers in high demand
- Clear shift toward IT-related positions

### Petition Numbers:

- Generally increasing annually (except 2020)
- Exceptional 2021 with almost 800,000 petitions
- Acceptance ratio consistently above 80%

### Wage Analysis:

- Median wage increases yearly (except 2022)
- Notable decrease in 2020
- Overall trend reflects salary growth

### Top Job Titles:

- Software Engineer and Software Developer dominate
- Information Technology fields dominate the top 10

### Classifier Accuracy:

- Random Forest, Logistic Regression, and Decision Tree exhibit consistent 96% accuracy

# Future Research

### 1. Explainable AI in H1B Visa Lottery Predictions:
- Develop and enhance explainable AI models that can provide clear insights into the factors influencing H1B visa lottery outcomes. This research is critical to ensure transparency in the decision-making process, helping both applicants and immigration officials understand the basis for lottery predictions.

### 2. Fairness and Bias Mitigation in Lottery Predictions:
- Investigate and address potential biases in H1B visa lottery prediction models. Ensuring fairness across demographic and socio-economic factors is crucial to prevent discrimination and promote an equitable distribution of visa opportunities. This research could involve the development of techniques to identify and mitigate biases in the prediction process.

### 3. Optimization Strategies for H1B Visa Applications:
- Explore optimization techniques that guide applicants in maximizing their chances of selection in the lottery. This research can involve the development of algorithms that analyze historical data and lottery criteria to provide recommendations for optimizing application submissions. Optimizing the application process can be valuable for both applicants and immigration authorities in managing the lottery efficiently.

