# Crowdfunding_ETL
Project 2
=======
## Group 4 Members:
Denis Kalala, 
Jay Boon, 
Kieran Nguyen, 
Alyssa Berridge,  
Esteban Ortega, 
Renz Supnet

#Notes
- When importing the data to the tables, please import the category, contacts, subcategory csvs first, before importing the campaign csv.

# Content breakdown for this repository
1. ERD folder with ERD diagram, QUickDBD diagram, and .sql file.
2. Resource folder with given Excel files and created CSV files
3. Jupyter Notebook file
4. Screenshots of succesfully created tables.

=======
##  Breakdown Project
1. Extract Data
- Load the crowdfunding.xlsx and contacts.xlsx files into Pandas DataFrames.

2. Transform Data
- Create the Category and Subcategory DataFrames
- Extract and transform the category & sub-category column.
- Generate unique category and subcategory IDs.
- Export the transformed data as category.csv and subcategory.csv.
- Create the Campaign DataFrame
- Extract relevant columns from crowdfunding.xlsx.
- Convert columns (goal, pledged, launch_date, end_date) to appropriate data types.
- Merge with category and subcategory DataFrames to assign IDs.
- Export as campaign.csv.

3. Create the Contacts DataFrame
  - Choose between dictionary methods or regular expressions to extract data.
  - Split the name column into first_name and last_name.
  - Convert contact_id to integer.
  - Export as contacts.csv.
   
4. Load Data into PostgreSQL
- Design an ERD and create a database schema in crowdfunding_db_schema.sql.
- Set up a PostgreSQL database named crowdfunding_db.
- Create tables using the schema.
- Import CSV files into corresponding tables.
- Run SELECT statements to verify the data.

# Usage Instructions
- Make sure psql is installed
- Open a terminal within the Resources directory
- Login into your psql account using the command ```psql -U (username)```
- Execute ```\i crowdfunding_db_schema.sql``` to run our sql code

# Resources 
- https://stackoverflow.com/questions/19231871/convert-unix-time-to-readable-date-in-pandas-dataframe (Converting unix time to readable date in pandas)
- https://stackoverflow.com/questions/13411544/delete-a-column-from-a-pandas-dataframe (Delete a column from a pandas dataframe)
