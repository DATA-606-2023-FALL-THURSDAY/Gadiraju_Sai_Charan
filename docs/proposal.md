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
- **Dataset Link**: [PERM Program - Fiscal Year 2022, 2021, 2020, 2019 Disclosure Files](https://www.dol.gov/agencies/eta/foreign-labor/performance)
- **Data Description**: The dataset consists of disclosure files for the PERM program, a labor certification program for employers seeking to hire foreign workers for permanent employment in the United States.

# Data

- The dataset consists of last four years information (2019-2022)
- Source: [Dataset Source](https://www.dol.gov/agencies/eta/foreign-labor/performance)  U.S. Department of Labor, ETA
- Data Size: 1069.51 MB
- Data Shape (Number of Rows and Columns): Number of rows: 1320781, Number of columns: 22
- Every row describes applicant information.
- Columns:
  - CASE_NUMBER - Unique identifier assigned to each application submitted for processing to OFLC.
  - DECISION_DATE - Date on which the determination was issued by OFLC.
  - CASE_STATUS - Status associated with the last significant event or decision. Valid values include “Certified”, “Certified-Expired”, “Denied”, and “Withdrawn”. 
  - REFILE - Identifies if application was previously filed. Y = Employer has previously submitted an Application. N = Employer has not previously submitted an Application. Form ETA-9089, Section A, Item 1. 
  - ORIG_FILE_DATE - Date application was originally filed (if applicable). Form ETA-9089, Section A, Item 1-A. 
  - SCHD_A_SHEEPHERDER - Identifies whether the application is in support of Schedule A or a Sheepherder Occupation. Y = Application is in support of a Schedule A or Sheepherder Occupation. N = Application is not in support of a Schedule A or Sheepherder Occupation. Form ETA-9089, Section B, Item 1. 
  - EMPLOYER_NAME - Legal business name of employer requesting permanent labor certification. Form ETA-9089, Section C, Item 1. 
  - EMPLOYER_ADDRESS_1 - Contact information of the employer requesting permanent labor certification. Form ETA-9089, Section C, Items 2 through 4. 
  - EMPLOYER_ADDRESS_2 
  - EMPLOYER_CITY
  - EMPLOYER_COUNTRY
  - EMPLOYER_POSTAL_CODE
  - EMPLOYER_PHONE
  - EMPLOYER_PHONE_EXT
  - EMPLOYER_NUM_EMPLOYEES - Total Number of employees employed by employer. Form ETA-9089, Section C, Item 5. 
  - FW_OWNERSHIP_INTEREST - Identifies if the foreign worker has an ownership interest or familial relationship with the Employer. Y = Foreign Worker has Ownership Interest; N = Foreign Worker has no Ownership Interest. Form ETA9089, Section C, Item 9. 
  - PW_SOC_CODE - Occupational code associated with the job being requested for permanent labor certification, as classified by the Standard Occupational Classification (SOC) System. Form ETA-9089, Section F, Item 2. 
  - PW_SOC_TITLE - Occupational title associated with the SOC/O*NET Code. Form ETA9089, Section F, Item 3. 
  - COUNTRY_OF_CITIZENSHIP - Country of citizenship of the foreign worker being sponsored by the employer for permanent employment in the United States.
  - CLASS_OF_ADMISSION - Indicates the current visa status of the foreign worker.
  - FOREIGN_WORKER_INFO_MAJOR - Major field(s) of study in reference to the highest level the foreign worker achieves.

### Target Variable- CASE_STATUS - Valid values include “Certified”, “Certified-Expired”, “Denied”, and “Withdrawn”

## Project Objective

The primary objective of this data science project is to explore, analyze, and gain insights from the PERM program disclosure data for the fiscal years 2022, 2021, 2020, and 2019. I aim to answer various research questions, uncover trends, and provide valuable information.

# Research Questions

- How the number of visa applications is increasing over the years (2019-2022).
- Top Companies offering H1B sponsorships.
- Key roles that are being offered Sponsorships.
- Salary distribution for the roles being offered.
- How the Data related roles look like.
- Acceptance and Rejection rate.
- Which part of the United States records more applications?
