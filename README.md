# Crowdfunding_ETL
---
## Objectives
The purpose of this project was to showcase the ETL workflow using tools and skills developed in this bootcamp.
We worked with 2 excel files, crodwfunding.xlsx and contacts.xlsx to complete the following instructions divided into 4 subsections

## Methodology
- Create the Category and Subcategory DataFrames
- Create the Campaign DataFrame
- Create the Contacts DataFrame
- Create the Crowdfunding Database

### 1-Creating the Category and Subcategory DataFrames
---
**In this section, we extracted and transformed the crowdfunding.xlsx Excel data to create a category DataFrame that has the following columns:**

- A "category_id" column that has entries going sequentially from "cat1" to "catn", where n is the number of unique categories
- A "category" column that contains only the category titles
  
**Then exported the category DataFrame as category.csv into a csv file.**

**Furthermore we created a subcategory DataFrame that has the following columns:**

- A "subcategory_id" column that has entries going sequentially from "subcat1" to "subcatn", where n is the number of unique subcategories
- A "subcategory" column that contains only the subcategory titles
  
**Finally we export the subcategory DataFrame as subcategory.csv and save it to your GitHub repository.**

#### 2-Creating the Campaign DataFrame
---
**In this section we have extracted and transformed the crowdfunding.xlsx Excel data to create a campaign DataFrame that has the following columns:**
* The "cf_id" column
* The "contact_id" column
* The "company_name" column
* The "blurb" column, renamed to "description"
* The "goal" column, converted to the float data type
* The "pledged" column, converted to the float data type
* The "outcome" column
* The "backers_count" column
* The "country" column
* The "currency" column
* The "launched_at" column, renamed to "launch_date" and with the UTC times converted to the datetime format
* The "deadline" column, renamed to "end_date" and with the UTC times converted to the datetime format
* The "category_id" column, with unique identification numbers matching those in the "category_id" column of the category DataFrame
* The "subcategory_id" column, with the unique identification numbers matching those in the "subcategory_id" column of the subcategory DataFrame
**Then exported the campaign DataFrame as campaign.csv into a csv file.**

#### 3-Creating the Contacts DataFrame
---
**In this portion,we chose Option 1: Use Python dictionary methods to extracting and transforming the data from the contacts.xlsx Excel data:**

- Import the contacts.xlsx file into a DataFrame.
- Iterate through the DataFrame, converting each row to a dictionary.
- Iterate through each dictionary, doing the following:
- Extract the dictionary values from the keys by using a Python list comprehension.
- Add the values for each row to a new list.
- Create a new DataFrame that contains the extracted data.
- Split each "name" column value into a first and last name, and place each in a new column.
- Clean and export the DataFrame as contacts.csv and save it to your GitHub repository.

#### 4-Creating the Crowdfunding Database
---
**For this last portion:**
- We inspected the four CSV files, and then sketched an ERD of the tables by using QuickDBD Links to an external site..
- Then used the information from the ERD to create a table schema for each CSV file.
- After that we created a new Postgres database, named crowdfunding_db.
- Furthermore , using the database schema, we created the tables in the correct order to handle the foreign keys.
- After verification of the table creation by running a SELECT statement for each table.
- We Imported each CSV file into its corresponding SQL table.
- Finally we verified that each table has the correct data by running a SELECT statement for each.


