# Crowdfunding_ETL
<strong>Module 13 Project 2 Extract, Load, Transform challenge for Data Analytics Bootcamp</strong>

<strong>FILES</strong>
<ul>
<li>ETL_Mini_Project_JBegley_VStyles.ipynb (<em>File</em>)
<li>Resources (<em>Directory</em>) - contacts.csv (<em>File</em>), contacts.xlsx (<em>File</em>), crowdfunding.csv (<em>File</em>), crowdfunding.xlsx (<em>File</em>), category.csv (<em>File</em>), subcategory.csv (<em>File</em>), campaign.csv (<em>File</em>)
<li>.ipynb_checkpoints (<em>Directory</em>) - ETL_Mini_Project_JBegley_VStyles-checkpoint.ipynb (<em>File</em>)</li>
</ul>

<strong>REQUIREMENTS</strong>
<ul>
<li>Create the Category and Subcategory DataFrames (30 points)
<li>Create the Campaign DataFrame (30 points)
<li>Create the Contacts DataFrame (15 points) - Option 1: Use Python dictionary methods
<li>Create the Crowdfunding Database (25 points)
</li>
</ul>

<strong>THE STEPS WE TOOK</strong><br>
<ul>
<li>The process was mostly straightforward with no major bugs.
<li>We noticed one error when creating the SQL schema, which was that the final campaign file had the wrong columns.
<li>We also had issues with merging files in GitHub, which we later resolved.
</ul>

PART 1: Create the Category and Subcategory DataFrames

1. Extract and transform the crowdfunding.xlsx Excel data to create a category DataFrame that has the following columns:

  * A "category_id" column that has entries going sequentially from "cat1" to "catn", where n is the number of unique categories,

  * A "category" column that contains only the category titles.

2. Export the category DataFrame as category.csv

3. Extract and transform the crowdfunding.xlsx Excel data to create a subcategory DataFrame that has the following columns:

  * A "subcategory_id" column that has entries going sequentially from "subcat1" to "subcatn", where n is the number of unique subcategories,

  * A "subcategory" column that contains only the subcategory titles.

4. Export the subcategory DataFrame as subcategory.csv

PART 2: Create the Campaign DataFrame

Create the Campaign DataFrame
1. Extract and transform the crowdfunding.xlsx Excel data to create a campaign DataFrame has the following columns:

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
    * 
    * 2.Export the campaign DataFrame as campaign.csv

PART 3: Create the Contacts DataFrame

1. We chose to extract and transform from the contacts.csv file with the use of Python dictionary method

    * Import the contacts.xlsx file into a DataFrame.
    * Iterate through the DataFrame, converting each row to a dictionary.
    * Iterate through each dictionary, doing the following:
        * Extract the dictionary values from the keys by using a Python list comprehension.
        * Add the values for each row to a new list.
    * Create a new DataFrame that contains the extracted data.
    * Split each "name" column value into a first and last name, and place each in a new column.
    * Clean and export the DataFrame as contacts_clean.csv 
    
    
PART 4: Create the Crowdfunding Database

1. Inspect the four CSV files, and then sketch an ERD of the tables by using QuickDBD Links to an external site. .
2. Use the information from the ERD to create a table schema for each CSV file. Note: Remember to specify the data types, primary keys, foreign keys, and other constraints.
3. Save the database schema as a Postgres file named crowdfunding_db_schema.sql, and save it to your GitHub repository.
4. Create a new Postgres database, named crowdfunding_db.
5. Using the database schema, create the tables in the correct order to handle the foreign keys.
6. Verify the table creation by running a SELECT statement for each table.
7. Import each CSV file into its corresponding SQL table.






<strong>ERD</strong><br>
![crowdfunding_ERD](https://user-images.githubusercontent.com/121570218/234084392-2ce36440-ca9e-44f7-a748-0368ac8efc44.png)
