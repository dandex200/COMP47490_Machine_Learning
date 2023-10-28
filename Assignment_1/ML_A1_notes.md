#[X]Task 1: Data Quality Plan
    **Features with Problems:**
        1. Rows with missing values in some columns
        2. Some columnes have values that are rounded to different places.
        3. Some column headers have spaces in them
    **Solutions:**
        1. Either impute or remove the rows with missing values. Test both and decide on which is better.
            Result: Impute kept statistics the same while Removing Missing Values changed all but max. 
        2. Identify majority number of decimal places and round all values to that place
            Result: Columns had values rounded to 8 decimal places. 
        3. Remove spaces from column titles/headers
            Result: Now no columns have un-needed whitespace. 
    **Explanation/Justification:**
        1. I chose to impute the missing values in each column rather than remove the rows with missing values as after testing each method, imputing kept the dataframes statistics (count, min, max, Q1, Median, and Q3) the same but removing rows changed all but max. This makes sense as it physically removed some data. This could lead to problems and false observations/results down the road in our further analysis as we will be performing operations on data with different statistics. 
        2. After reviewing the dataset manually, I noticed quite a few columns had values with different counts of decimal places. To make all of the data uniform so no potential issues rise later on, I decided to average the amount of decimal places and round all values to that count (of 8). 
        3. During the coding of checking number of decimal places, I noticed an error in the column title/headers- the 8 descriptive feature columns have whitespace before the first word- a potential error for plotting/analysis further down. To fix this I simply removed that whitespace from the first 8 columns. 
#[ ]Task 2: Normalize or Standardize 
    **Normalization or Standardization and why?:**
        * s

# [ ]Task 3: Decide the Evaluation Measure. Justify - why?


#[ ]Task 4: 

#[ ]Task 5: 

#[ ]Task 6: 

#[ ]Task 7: 

#[ ]Task 8: 

#[ ]Task 9(Bonus): 
