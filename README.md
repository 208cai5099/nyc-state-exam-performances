# NYC State Exam Performances

## Introduction
New York City (NYC) has over 700 public elementary and middle schools spread out across 32 geographic school districts. The city is composed of 5 boroughs: Manhattan, Brooklyn, Bronx, Staten Island, and Queens. Every year, millions of students take the annual state exams in ELA and math to assess their learning progress in fundamental literacy and math skills. The results of the exams are published on [NYC Public Schools InfoHub](https://infohub.nyced.org/reports/academics/test-results) for the general public. The results are presented as Excel files. The use of Excel files can make it harder for some families and students to access and interpret the data. Some people are not familiar with Excel, and the Excel file containing school-level data is too large for some computers to open smoothly. This poses a challenge for families and students who want to learn about the school performance data.

## Purpose
The purpose of this project is to create an online dashboard that displays the performances of NYC schools on the 2023 and 2024 state exams. The dashboard has the following features:

* Displays the percentages of students scoring in each of the performance levels from 1 to 4 (level 3 and 4 are considered proficient)
* Displays the differences between school-level proficiency rate and district-level proficiency rate
* Displays the differences between school-level proficiency rate and borough-level proficiency rate

The dashboard is intended to be a user-friendly tool to explore the performances of schools in NYC. Because the dashboard can easily be accessed in a web browser, it provides easy and fast access to school performance data for the general public.

The dashboard can be accessed here: https://lookerstudio.google.com/reporting/31445d1a-bc55-4c22-8020-7ec4d2134048

**Disclaimer: The information in this dashboard are intended for informative purposes only. Please do not use the provided information as advice for school applications.**

![Screenshot 2025-05-01 at 1 01 14 AM](https://github.com/user-attachments/assets/3bbec0e2-98a8-4158-9bcf-6cb13be7917f)

## Methods
The data files are downloaded from NYC Public Schools InfoHub (last downloaded in April 2025). The files are parsed using Python, and the data are re-organized in a specific format. The processed data are stored on Google's BigQuery platform. The dashboard is designed in Looker Studio that accesses the data from BigQuery.

## Notes
As stated in the downloaded data files, there are a few limitations in the data. 

District 75 is a set of schools that provide instruction to students with extensive learning needs. It is not a geographic school district. District 75 schools are distributed across the geographic school districts in the city. The data from District 75 schools are excluded from the school-level and borough-level data files. The data files do not display the performance data of individual District 75 schools, and the borough proficiency rates (level 3 and level 4 combined) do not take into account of District 75 schools. However, District 75 schools are included in the district-level proficiency rates, respective to their geographic school districts.

If a school has a small enough number of test takers, their performance results are redacted in the data files. This might limit the insight into school performance.
