# nosql_analysis

## Eat Safe, Love

![image](https://user-images.githubusercontent.com/119654958/225827150-76bff523-fbdb-406b-ae3a-1a93beeba37e.png)

## Part 1: Database and Jupyter Notebook Set Up

- Used NoSQL_setup.ipynb for this section of the analysis.

- Imported the data provided in the establishments.json file from Terminal. Named the database uk_food and the collection establishments. 

- Within your notebook, imported the libraries needed: PyMongo and Pretty Print (pprint).

- Created an instance of the Mongo Client.

- Confirmed that I created the database and loaded the data properly.

- Assign the establishments collection to a variable to prepare the collection for use.

## Part 2: Update the Database

Made the following changes to the establishments collection:

- Found the BusinessTypeID for "Restaurant/Cafe/Canteen" and returned only the BusinessTypeID and BusinessType fields.

- Updated the new restaurant with the BusinessTypeID found.

- Removed any establishments within the Dover Local Authority from the database, and checked the number of documents to ensure they were deleted.

- Used update_many to convert latitude and longitude to decimal numbers.

## Part 3: Exploratory Analysis

Used NoSQL_analysis_starter.ipynb for this section of the challenge.

Some notes to be aware of while you are exploring the dataset:

- RatingValue refers to the overall rating decided by the Food Authority and ranges from 1-5. The higher the value, the better the rating. Note: This field also includes non-numeric values such as 'Pass', where 'Pass' means that the establishment passed their inspection but isn't given a number rating.

- The scores for Hygiene, Structural, and ConfidenceInManagement work in reverse. This means, the higher the value, the worse the establishment is in these areas.

For each question:

- Used count_documents to display the number of documents contained in the result.

- Displayed the first document in the results using pprint.

- Converted the result to a Pandas DataFrame, print the number of rows in the DataFrame, and display the first 10 rows.
 
 # Answered the following questions: 
 
 Which establishments have a hygiene score equal to 20?

Which establishments in London have a RatingValue greater than or equal to 4?

What are the top 5 establishments with a RatingValue of '5', sorted by lowest hygiene score, nearest to the new restaurant added, "Penang Flavours"?

How many establishments in each Local Authority area have a hygiene score of 0? Sorted the results from highest to lowest, and printed out the top ten local authority areas.

![image](https://user-images.githubusercontent.com/119654958/225828287-88e9c08e-e581-4732-b1a8-7fd39656e158.png)
