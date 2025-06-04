

This repository contains a series of tasks I completed as part of my work with Commonwealth Bank’s Data Science team. Throughout this project, I demonstrated my expertise in data management, data analysis, and database design, focusing on real-world data science challenges such as aggregation, anonymization, social media analysis, and structuring complex datasets. 

The tasks encompass key aspects of data science workflows, including the creation of data engineering pipelines, the application of data privacy techniques, and the design of robust systems for managing and analyzing social media data. Each task involved critical thinking and proficiency in using data-driven decision-making processes to meet business objectives.

## Table of Contents
- [Introduction](#introduction)
- [Role Overview](#role-overview)
- [Task 1: Data Aggregation and Analysis](#task-1-data-aggregation-and-analysis)
- [Task 2: Data Anonymization](#task-2-data-anonymization)
- [Task 3: Data Analysis Proposal](#task-3-data-analysis-proposal)
- [Task 4: Database Design Proposal](#task-4-database-design-proposal)
- [Usage](#usage)
- [Contributing](#contributing)
- [License](#license)

---

## Introduction
The tasks in this repository demonstrate how I applied my data science skills to support the Commonwealth Bank’s Data Science team in optimizing operational and business decisions through effective data management and analysis. These tasks were designed to align with real-world applications where data privacy, accurate analysis, and data engineering are crucial for the bank's operations. The repository showcases my ability to clean and analyze large datasets, anonymize sensitive customer data to meet privacy regulations, propose actionable insights for business use, and create a structured database system for long-term data storage and analysis.

---

## Role Overview
In my capacity as a **Data Scientist**, I was entrusted with several key tasks that required me to demonstrate my proficiency in:

1. **Data Engineering**: Creating efficient data pipelines to aggregate and process raw transactional data for downstream analysis.
2. **Data Anonymization**: Ensuring that sensitive customer information was anonymized to meet privacy standards while retaining the usefulness of the data for analytical purposes.
3. **Social Media Analysis Proposal**: Developing strategies for extracting actionable insights from social media interactions, specifically from Twitter, to inform marketing and customer engagement strategies.
4. **Database Design**: Designing a structured database schema to efficiently store and manage data for long-term use, ensuring ease of retrieval and scalability.

Throughout these tasks, I applied a variety of data science methodologies and tools, including data aggregation, SQL scripting, anonymization techniques, and database normalization, all while adhering to privacy regulations like GDPR.

---

## Task 1: Data Aggregation and Analysis

### Overview
In Task 1, I was provided with transactional data from various supermarkets across Australia, specifically within the `supermarket_transactions.csv` file. The objective was to clean, aggregate, and analyze the data to answer key business questions. The primary questions were:

1. **How many apples were purchased in cash across various locations?**
2. **How much money was spent on apples using cash?**
3. **How much money was spent at the Bakershire store by non-member customers across all payment methods?**

### Files:
- **supermarket_transactions.csv**: Raw transactional data provided for the analysis.
- **Apple_&_Bakershire_Transaction_Analysed.xlsx**: The analyzed dataset that contains answers to the business questions, including formulas used for calculations.
- **apple_and_bakershire_transactions_analysed_in_sql.sql**: SQL script that performs the same analysis as in Excel, demonstrating the application of data aggregation techniques in a relational database.
- **complete_model_csv.csv**: Final processed data file containing all aggregated results for easy review.
- **Data Aggregation and Analysis.xlsx**: Excel workbook with detailed analysis, including all aggregation steps and calculations.
- **Data Aggregation.txt**: A text file explaining the methods used for aggregating the data, including formula descriptions and steps taken.

### Methodology:
To answer the questions, the following steps were performed:

- **Data Cleaning**: Loaded the data into Excel and performed initial cleaning, filtering out any rows with missing or irrelevant data.
- **Aggregation**: Utilized Excel formulas such as `SUMIFS`, `COUNTIFS`, and filtering to aggregate and compute the required metrics.
- **SQL Analysis**: Replicated the Excel analysis using SQL queries to demonstrate the same results in a database environment, ensuring scalability for larger datasets.
- **Data Summation**: Summed up the total quantities and amounts for apples purchased in cash and the total spent at Bakershire by non-members.

---

## Task 2: Data Anonymization

### Overview
In Task 2, I was tasked with anonymizing sensitive customer information to ensure compliance with data privacy regulations while preserving the usefulness of the data for analysis. The dataset `mobile_customers.csv` contained personal identifiers such as customer names, phone numbers, and emails, which needed to be anonymized before sharing with InsightSpark for analysis.

### Files:
- **mobile_customers.csv**: Raw customer data containing personally identifiable information (PII).
- **masking_mobile_customers.csv**: Anonymized dataset with sensitive information removed or replaced with random or fake data.

### Methodology:
The anonymization process involved several steps to mask or replace sensitive data:

- **Removal of Non-Essential Columns**: Removed columns such as `customer_id` and `current_location`, which were deemed non-essential for analysis.
- **Data Masking**: Replaced actual customer names and email addresses with fake names and masked emails using a consistent pattern.
- **Noise Addition**: Introduced noise in the `date_registered` and `birthdate` fields by adding random offsets to protect real values.
- **Categorization**: Grouped continuous variables like `age` and `salary` into predefined categories (e.g., age groups, salary bands) to obscure exact values.
- **Tokenization**: Tokenized categorical data such as `credit_card_provider`, `credit_card_expiry`, and `job_title` to protect specific details while retaining data utility.

---

## Task 3: Data Analysis Proposal

### Overview
In Task 3, I was tasked with proposing data analysis strategies for extracting actionable insights from CommBank’s Twitter account. The goal was to identify opportunities for improving marketing and customer engagement by analyzing tweet data and interactions from users.

### Files:
- **Proposal_for_Data_Analysis_Approaches.pdf**: A detailed document outlining the methods for analyzing Twitter data, including strategies for sentiment analysis, user engagement evaluation, and trend identification.

### Proposed Methods:
- **Sentiment Analysis**: Analyze replies, retweets, and mentions to assess customer sentiment (positive, negative, or neutral) towards CommBank.
- **Engagement Metrics**: Study user interactions such as likes, retweets, and replies to identify which tweets generate the most engagement.
- **Trend Analysis**: Evaluate tweet timing, content, and frequency to identify optimal posting strategies for better engagement.
- **Audience Profiling**: Analyze the profiles of users engaging with CommBank’s Twitter to uncover demographic insights and tailor marketing strategies.

---

## Task 4: Database Design Proposal

### Overview
In Task 4, I was responsible for designing a database schema to store and manage Twitter data. The schema had to accommodate tweet content, user interactions (replies, retweets, mentions), and engagement metrics while ensuring scalability and efficient querying for future analysis.

### Files:
- **Proposal_for_Designing_a_Database_to_Store_CommBank_Twitter_Data.pdf**: A proposal document that outlines the database structure, including table design, relationships, and indexing strategies.

### Approach:
- **Table Design**: Designed tables for storing tweet data (`tweets` table), user replies (`replies` table), mentions (`mentions` table), and user profiles (`users` table).
- **Primary Keys**: Defined primary keys for each table to uniquely identify each record (e.g., `tweet_id`, `user_id`).
- **Relationships**: Established relationships between tables to allow efficient retrieval of related data (e.g., linking tweets to users and user profiles).
- **Normalization**: Applied database normalization principles to ensure minimal redundancy and preserve data integrity.
- **Indexing**: Suggested indexing on frequently queried fields (e.g., `tweet_id`, `user_id`, `timestamp`) to improve query performance.

---

## Usage


1. **File Navigation:**
   - **Task 1**: Open `supermarket_transactions.csv` in Excel or any spreadsheet program to view the raw data. The `Apple_&_Bakershire_Transaction_Analysed.xlsx` file contains the detailed analysis and results.
   - **Task 2**: Explore the anonymized `masking_mobile_customers.csv` file to understand the anonymization techniques applied to the customer data.
   - **Task 3**: Read the `Proposal_for_Data_Analysis_Approaches.pdf` to explore the strategies I proposed for analyzing Twitter data.
   - **Task 4**: View the `Proposal_for_Designing_a_Database_to_Store_CommBank_Twitter_Data.pdf` to understand the database schema and structure.

---


## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
