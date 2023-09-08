# Title and Author

- **Project Title**: Data Analysis for H1B VISA
- **Prepared for UMBC Data Science Master Degree Capstone by**: Dr. Chaojie (Jay) Wang
- **Author**: Gadiraju Sai Charan
- **Link to the author's GitHub profile**: [GitHub Profile](https://github.com/Saicharan0297)
- **Link to the author's LinkedIn profile**: [LinkedIn Profile](https://www.linkedin.com/in/sai-charan-gadiraju/)
- **Link to PowerPoint presentation file**: Will update later 
- **Link to Youtube Video**: Will Update later

# Background

For this data science final project, I will analyze the PERM (Program Electronic Review Management) disclosure files provided by the U.S. Department of Labor's Employment and Training Administration (ETA). These disclosure files contain valuable information about foreign labor certification programs in the United States.

### Data Source
- **Data Provider**: U.S. Department of Labor, ETA
- **Dataset Link**: [PERM Program - Fiscal Year 2022, 2021, 2020, 2019 Disclosure Files](https://www.dol.gov/agencies/eta/foreign-labor/performance)
- **Data Description**: The dataset consists of disclosure files for the PERM program, a labor certification program for employers seeking to hire foreign workers for permanent employment in the United States.

# Data

- The dataset consists of last four years information (2019-2022)
- Source: [Dataset Source](https://www.dol.gov/agencies/eta/foreign-labor/performance)
- Data Size: 1069.51 MB
- Data Shape (Number of Rows and Columns): Number of rows: 1320781, Number of columns: 22
- Columns:
  CASE_NUMBER - Unique identifier assigned to each application submitted for processing to OFLC.
  DECISION_DATE - Date on which the determination was issued by OFLC.
  CASE_STATUS - Status associated with the last significant event or decision. Valid values include “Certified”, “Certified-Expired”, “Denied”, and “Withdrawn”. 
  REFILE - Identifies if application was previously filed. Y = Employer has previously submitted an Application. N = Employer has not previously submitted an Application. Form ETA-9089, Section A, Item 1. 
  ORIG_FILE_DATE - Date application was originally filed (if applicable). Form ETA-9089, Section A, Item 1-A. 
  SCHD_A_SHEEPHERDER - Identifies whether the application is in support of Schedule A or a Sheepherder Occupation. Y = Application is in support of a Schedule A or Sheepherder Occupation. N = Application is not in support of a Schedule A or Sheepherder Occupation. Form ETA-9089, Section B, Item 1. 
  EMPLOYER_NAME - Legal business name of employer requesting permanent labor certification. Form ETA-9089, Section C, Item 1. 
  EMPLOYER_ADDRESS_1 - Contact information of the employer requesting permanent labor certification. Form ETA-9089, Section C, Items 2 through 4. 
  EMPLOYER_ADDRESS_2 
  EMPLOYER_CITY
  EMPLOYER_COUNTRY
  EMPLOYER_POSTAL_CODE
  EMPLOYER_PHONE
  EMPLOYER_PHONE_EXT
  EMPLOYER_NUM_EMPLOYEES - Total Number of employees employed by employer. Form ETA-9089, Section C, Item 5. 
  FW_OWNERSHIP_INTEREST - Identifies if the foreign worker has ownership interest or familial relationship with the Employer. Y = Foreign Worker has Ownership Interest; N = Foreign Worker has no Ownership Interest. Form ETA9089, Section C, Item 9. 
  PW_SOC_CODE - Occupational code associated with the job being requested for permanent labor certification, as classified by the Standard Occupational Classification (SOC) System. Form ETA-9089, Section F, Item 2. 
  PW_SOC_TITLE - Occupational title associated with the SOC/O*NET Code. Form ETA9089, Section F, Item 3. 
  COUNTRY_OF_CITIZENSHIP - Country of citizenship of the foreign worker being sponsored by the employer for permanent employment in the United States.
  CLASS_OF_ADMISSION - Indicates the current visa status of the foreign worker.
  FOREIGN_WORKER_INFO_MAJOR - Major field(s) of study in reference to the highest level achieved by the foreign worker.

## Project Objective

The primary objective of this data science project is to explore, analyze, and gain insights from the PERM program disclosure data for the fiscal years 2022, 2021, 2020, and 2019. I aim to answer various research questions, uncover trends, and provide valuable information.

# Research Questions

1. Trend Analysis:

What is the trend in the number of PERM applications filed over the selected fiscal years?
Can we identify any seasonality or long-term trends in application submissions?

2. Approval Rates Over Time:

How have the approval rates for PERM applications changed from 2019 to 2022?
Are there any noticeable variations in approval rates across different industries or regions?

3. Processing Time Trends:

Is there a trend in the average processing time for PERM applications?
Have processing times improved or worsened over the years?

4. Industry Insights:

Which industries have the highest and lowest certification rates?
Can we visualize the distribution of approved applications across various sectors?

5. Geographical Analysis:

What are the top states with the highest number of PERM applications?
Are there states where the approval rates significantly differ from the national average?

6. Top Occupations:

Which job categories consistently receive the most certifications?
Can we visualize the top occupations that foreign workers are hired for?

7. Wage Distribution:

How does the wage distribution vary across different job categories?
Are there job categories where the offered wages tend to be higher or lower?

8. Country of Origin:

What are the primary countries of origin for foreign workers in PERM applications?
Can we visualize the diversity in the nationalities of foreign workers?

9. Processing Times by Country:

Are there significant differences in processing times for applications from specific countries?
Can we visualize the average processing times by country of the foreign worker?

10. Impact of Visa Preference:

How does the choice of visa preference category affect approval rates?
Are certain preference categories more likely to lead to certification?

11. Changes Over Fiscal Years:

Can we identify any noteworthy changes in the data trends or patterns between 2019 and 2022?
Are there any outliers or anomalies in specific years that require investigation?

12. Correlation Analysis:

Is there a correlation between factors like offered wages and approval rates?
Can we identify any strong relationships between variables using correlation matrices?

13. Visualization of Denials:

Visualize the reasons for application denials or withdrawals, highlighting common issues.
Are there trends in the types of documentation problems leading to denials?

14. Policy Analysis:

Use visualizations to highlight policy changes over the years and their potential impact on certification rates.
Are there notable changes in the data coinciding with specific policy changes?

15. Interactive Dashboards:

Create interactive dashboards to allow users to explore the data, filter by various criteria, and gain insights on-demand.
