Overview
A complete Data Cleaning & Preprocessing pipeline built on raw, messy internship application data. Covers every real-world data quality issue — missing values, duplicates, outliers, inconsistent formatting — and produces a clean, analysis-ready dataset.

Objective
Transform raw, unreliable data into a clean, structured, and consistent dataset ready for analysis or ML modeling.

Problems Found in Raw Data
ProblemExampleDuplicate rowsSame application submitted multiple timesMissing valuesage, gpa, city fields left emptyInconsistent casingtech, TECH, Tech all meaning the sameOutliersage = 999, gpa = 5.5, salary = -5000Invalid phone numbersabc, 123 stored as phoneInvalid dates99-99-9999, not a dateExtra whitespace"  Applicant_1  " instead of "Applicant_1"

Cleaning Steps
StepTask1Remove duplicate rows2Standardize text — strip spaces, fix casing, fix abbreviations3Fill missing numeric values with median4Fill missing categorical values with mode5Fix outliers using clipping (valid range enforcement)6Validate phone numbers using Regex7Parse and fix invalid dates using pd.to_datetime8Correct data types for all columns9Engineer 4 new features from existing data

New Features Added
FeatureDescriptiongpa_categoryExcellent / Good / Average / Below Averageexperience_levelFresher / Junior / Mid-Level / Seniorapplication_yearExtracted from application dateapplication_monthExtracted from application date

Results
MetricBeforeAfterTotal Rows220200Duplicates200Missing Values45+0Invalid OutliersMultiple0Features1216

Key Takeaway
Raw data is never ready for analysis. A proper cleaning pipeline ensures reliable, consistent, and trustworthy results — this is the foundation of every Data Analyst's work.
