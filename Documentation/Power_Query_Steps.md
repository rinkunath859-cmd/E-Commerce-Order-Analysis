# Power Query Transformations

•This document describes all data preparation and transformation steps performed in Power Query Editor before loading the data into the Power BI data model.

Step 1: Import the Excel Workbook
Open Power BI Desktop.
Go to Home → Get Data → Excel Workbook.
Browse and select the Excel file.
Select the following tables:
Orders
Customers
Sales Targets
Click Transform Data to open Power Query.
Step 2: Clean the Orders Table
2.1 Rename the Query

Rename the imported query to:

Orders
2.2 Check Data Types

Verify that each column has the correct data type.

Column	Data Type
Order ID	Text
Customer ID	Text
Order Datetime	Date/Time
Order Source	Text
Sales POC	Text
Order Value	Decimal Number
2.3 Remove Duplicate Records
Select Order ID.
Go to Home → Remove Rows → Remove Duplicates.

Since Order ID is unique, this ensures no duplicate transactions exist.

2.4 Identify Missing Values

Select the Order Source column.

Use the filter to display only (null) values.

This identifies all records affected by the system bug.

2.5 Determine the Bug Duration

Sort Order Datetime in ascending order.

Record:

First timestamp with missing Order Source.
Last timestamp with missing Order Source.

This defines the period during which the system failed to capture the sales channel.

2.6 Handle Missing Values

Replace missing values using one of the following approaches:

Option A – Fill Down (if missing values occur in one continuous period):

Select Order Source.
Go to Transform → Fill → Down.

Option B – Replace with Mode (if missing values are scattered):

Replace null values with the most frequently occurring Order Source.

Reason: Order Source is a categorical field, so mode or Fill Down is more appropriate than numerical imputation methods.

2.7 Verify Data Quality

Check that:

Order ID values are unique.
Customer IDs are populated.
Sales POC values are not blank.
Order Value contains no negative values.
Step 3: Clean the Customers Table
3.1 Rename the Query

Rename the query to:

Customers
3.2 Check Data Types
Column	Data Type
Customer ID	Text
Gender	Text
Age	Whole Number
Country	Text
Category	Text
3.3 Remove Duplicate Customers

Select Customer ID.

Go to:

Home → Remove Rows → Remove Duplicates

This ensures each customer appears only once.

3.4 Handle Missing Values

Inspect each column for null values.

If found:

Fill text columns where appropriate.
Remove records with invalid Customer IDs if necessary.
3.5 Validate Customer Information

Confirm:

Age values are reasonable.
Gender values are consistent.
Country names are standardized.
Category names contain no spelling inconsistencies.
Step 4: Clean the Sales Targets Table
4.1 Rename the Query

Rename the query to:

Sales Targets
4.2 Check Data Types
Column	Data Type
Sales POC	Text
Sales Manager First Name	Text
Sales Manager Last Name	Text
Sales Team	Text
Sales Target	Decimal Number
4.3 Create Sales Manager Column

Select:

Sales Manager First Name
Sales Manager Last Name

Go to:

Transform → Merge Columns

Separator:

Space

New column name:

Sales Manager

Example:

Rahul Sharma
4.4 Remove Unnecessary Columns

If the project only requires the merged Sales Manager field, remove:

Sales Manager First Name
Sales Manager Last Name
4.5 Verify Sales Targets

Ensure:

Each Sales POC has a target.
Sales Team values are populated.
Sales Target values are numeric and non-negative.
Step 5: Final Data Validation

Review all queries to ensure:

No duplicate records.
Correct data types.
Missing values handled.
Consistent naming conventions.
Clean and accurate data.
Step 6: Load Data

Click:

Home → Close & Apply

Power BI loads the cleaned tables into the data model.

Summary of Power Query Transformations
Table	Transformation
Orders	Corrected data types
Orders	Removed duplicate Order IDs
Orders	Identified missing Order Source values
Orders	Filled missing Order Source values
Orders	Verified Order DateTime and Order Value
Customers	Corrected data types
Customers	Removed duplicate Customer IDs
Customers	Validated Age, Gender, Country, and Category
Sales Targets	Corrected data types
Sales Targets	Merged First Name and Last Name into Sales Manager
Sales Targets	Validated Sales Targets and Sales Team information
All Tables	Performed final data quality checks
Outcome

After completing these Power Query transformations:

The dataset is clean, consistent, and analysis-ready.
Missing values are handled appropriately.
Duplicate records are removed.
Sales Manager information is consolidated into a single field.
The cleaned tables are ready for relationship creation, DAX calculations, and dashboard development in Power BI.
