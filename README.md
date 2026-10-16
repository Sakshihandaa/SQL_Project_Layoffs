# Tech_Layoffs_Dataset_Analysis

## World Tech Layoffs Exploration and Data Cleaning with SQL

Most of us are aware of the massive global wave of tech industry workforce reductions over recent years. The idea of analyzing the World Tech Layoffs dataset is to get an overview of what actually happened across companies, industries, countries and funding stages between 2020 and 2023. The dataset consists of over 2,300 rows with columns such as `company`, `location`, `industry`, `total_laid_off`, `percentage_laid_off`, `date`, `stage`, `country` and `funds_raised_millions`.

While Exploring and Cleaning Data with SQL, I worked on the following things...
1. Created staging tables (`layoffs_staging` and `layoffs_staging2`) to safely transform and clean data without altering raw source files.
2. Identified and deleted duplicate records using SQL Window Functions.
3. Standardized inconsistent category values.
4. Trimmed trailing punctuation and whitespaces from text columns like `country`.
5. Converted text date strings into standard SQL data types.
6. Handled blank strings and `NULL` values by writing Self-Joins to populate missing records from existing company entries.
7. Filtered and purged non-actionable records where both `total_laid_off` and `percentage_laid_off` were missing.
8. Performed exploratory analysis using Window Functions, CTEs, rolling monthly totals and multi-level groupings.

---

After Data Exploration with SQL, I started working on Analyzing the Data with SQL where I found insights such as...
1. According to this dataset, the United States accounts for 66.38% of total recorded tech layoffs worldwide (256,474 employees), followed by India with 9.32% (35,993 employees).
2. Tech layoffs peaked dramatically between 2022 and early 2023, accounting for over 288,000 total workforce reductions compared to 81,068 in 2020 and 15,823 in 2021.
3. Among all tech sectors, Consumer tech suffered the highest overall workforce reduction (46,682 layoffs), followed closely by Retail (43,613 layoffs) and Transportation (31,998 layoffs).
4. Amazon recorded the highest cumulative workforce reduction of any individual company in the dataset (18,150 total employees laid off across multiple rounds).
5. The top 5 companies with the largest overall layoffs are Amazon (18,150), Google (12,000), Meta (11,000), Salesforce (10,090) and Philips (10,000).
6. Out of all funding stages, Post-IPO companies accounted for the overwhelming majority of workforce downsizing compared to early-stage or private venture-backed startups.
7. Several companies laid off 100% of their staff, with the highest-funded among them raising hundreds of millions prior to shutting down operations.
8. The single largest individual layoff event recorded occurred in early 2023 when Google reduced its global workforce by 12,000 employees in a single round.
