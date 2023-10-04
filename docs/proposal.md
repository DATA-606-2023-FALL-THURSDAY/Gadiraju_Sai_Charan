# Title and Author

- **Project Title**: H1B VISA Data Analysis 
- **Prepared for UMBC Data Science Master Degree Capstone by**: Dr. Chaojie (Jay) Wang
- **Author**: Gadiraju Sai Charan
- **Link to the author's GitHub profile**: [GitHub Profile](https://github.com/Saicharan0297)
- **Link to the author's LinkedIn profile**: [LinkedIn Profile](https://www.linkedin.com/in/sai-charan-gadiraju/)
- **Link to PowerPoint presentation file**: Will update later 
- **Link to Youtube Video**: Will Update later

# Background

For this final project, I will analyze the PERM (Program Electronic Review Management) disclosure files provided by the U.S. Department of Labor's Employment and Training Administration (ETA). These disclosure files contain valuable information about foreign labor certification programs in the United States.

## What is H-1B VISA?
- H-1B visas are a category of employment-based, non-immigrant visas for temporary foreign workers in the United States. 
- For a foreign national to apply for H1-B visa, a US employer must offer them a job and submit a petition for a H-1B visa to the US immigration department. 
- This is also the most common visa status applied for and held by international students once they complete college or higher education and begin working in a full-time position.
- The duration of stay is three years, extendable to six years, after which the visa holder may need to reapply.

## Quick facts about H1B Visa lottery:

- The Immigration Act of 1990 established a limit of 65,000 foreign nationals who may be issued a visa each fiscal year.
- An additional 20,000 H-1Bs are available to foreign nationals holding a master's or higher degree from U.S. universities.
- In addition, excluded from the ceiling are all H-1B non-immigrants who work at universities, non-profit research facilities associated with universities, and government research facilities.
- Person in H-1B status must continue to be employed by their employer in order to stay in H-1B status. If the person's employment ends for any reason, the person must leave the United States, unless the person is granted a change of status or finds another employer compatible with the H-1B status.
- The United States Citizenship and Immigration Services allows grace period of up to 60 days to stay in the United States after the person's end of employment.

### Data Source
- **Data Provider**: U.S. Department of Labor, ETA
- **Dataset Link**: [PERM Program - Fiscal Year 2022, 2021, 2020, 2019 Disclosure Files]([https://www.dol.gov/agencies/eta/foreign-labor/performance](https://www.kaggle.com/datasets/jishnukoliyadan/lca-programs-h1b-h1b1-e3-visa-petitions))
- **Data Description**: The dataset consists of disclosure files for the PERM program, a labor certification program for employers seeking to hire foreign workers for permanent employment in the United States.

# Data

- The dataset consists of last four years information (2019-2022)
- Source: [Dataset Source]([https://www.dol.gov/agencies/eta/foreign-labor/performance](https://www.kaggle.com/datasets/jishnukoliyadan/lca-programs-h1b-h1b1-e3-visa-petitions))  U.S. Department of Labor, ETA
- Data Size: 454.7+ MB
- Data Shape (Number of Rows and Columns): Number of rows: 3973349, Number of columns: 14
- Every row describes applicant information.
- Columns:
  Visa_Class -  It typically refers to the category or type of visa an individual is applying for, such as H-1B, H-1B1, E-3, etc.
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

The primary objective of this data science project is to explore, analyze, and gain insights from the PERM program disclosure data for the fiscal years 2022, 2021, 2020, and 2019. I aim to answer various research questions, uncover trends, and provide valuable information.

# Research Questions

"What are the trends and patterns in H1B visa applications in the United States from 2017 to 2022, focusing on factors such as the overall growth in the number of applications, the top companies providing H1B sponsorships, key roles in demand, salary distributions for these roles, characteristics of data-related roles, acceptance and rejection rates, and geographical concentrations of applications across different parts of the United States?"
