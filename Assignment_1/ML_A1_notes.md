#[XXX]Task 1: Data Quality Plan
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
#[X]Task 2: Normalize or Standardize 
    **Normalization or Standardization and why?:**
        * After test-applying normalization and standardization to the dataframe, I 

#[ ]Task 3: Decide the Evaluation Measure. Justify - why?
    **Which Evaluation Measure? Why?**
        Let's remind ourselves what we will be evaluating- detected signals and 8 different feature classes showing attributes of these detected signals. 
    
#[XXX]Task 4: 
    **Observation of a decision tree Classifer based on F1-Score**
    
    **Observation of kNN Classifer based on F1-Score**
    
    **Observation of SVM-Linear based on F1-Score**
    
    **Observation of SVM-Poly based on F1-Score**
    
    **Observation of SVM-RBF based on F1-Score**
    
    **Observation of SVM-Sigmoid based on F1-Score**
    
    **Winner Classifier/Parameter Setting:**
    
    **Why did we get those comparison results?**
    
    **Surprised at relative performance of linear, rbf and sigmoid kernels?**
    
    Notes
        * Test/train sets
        
        The above dictiionary printout shows a sorted compilation of 6 classifiers we used on our dataset's features. Decission Tree and kNN both were the most accurate. Then you could classify SVNM with a POLY or RBF kernel as the second best group of classiifers, with the SVM kernel's LINEAR and SIGMOID being the worst of these 6 in classification. These were ranked by finding the F SCORE of their classifcation and sorting them in descending order. The evaluation measure of analyzing the F score was previously selected in Task 3. The Winner Classifer/Parameter Seting is **Decision Tree Classifier** with parameters (criterion='entropy', max_depth=3) with an F Score of **0.8771407297096053**.

        I used the method of splitting the dataset into training/test sets as it easily lets us test our results with another group so we can double check our data is accurate easily. 

        I believe I received these comparison results of non SVM classifers being more accurate than the SVM classifers as SVM tends to handle linear values better while Decision Tree and kNN classifiers tend to handle non-linear values better. Our dataset seemingly has greater non-linear values. 

        I am surprised that only SVM: Linear and SVM: Sigmoid performed so poorly, their values are signficantly less accurate (20-40%) than the other 4 classifers. They seem to not be useful at all for our dataset and should be avoided. 
#[XXX]Task 5: 
        The top scores of the dictionary we output in Task 4 were all either DCT or kNN (two classifiers we didn't do in task), I will compare this output dictionary to rows starting in 5 in the previous task. It follows the same trend of RBF and POLY being the top 2 SVM classifiers and LINEAR and SIGMOID being less accurate. 
#[XXX]Task 6: 
        Unfortunately, I was only able to run two different classifiers (out of original 6) with this feature selection method (RFE) due to receiving an error I did not fix (relating to coef_ and feature_importances_). 
        These two feature selection methods provided us with their top 3 selected features, similarly to in Task 5 how we chose discriminative features by sorting the output of a variance method. 
        First, they each read in their respective model (either DCT or SVM:Linear in this case). Then, the wrapper feature selection technique I chose (Recrusive Feature Elimination) was fed the model and an input number of features to select (3 as in the top 3 we did in task 5). 
        After that, it is fit with the training sets from X and y as defined previously along with needed columsn. Then the final dataframes of selected features are loaded and we can see that the the top 3 features from the Decision Tree Classifier and RFE are: 'Excess kurtosis of the integrated profile', 'Skewness of the integrated profile', and 'Mean of the DM-SNR curve'. The top 3 features from the SVM:Linear classifer are 'Mean of the integrated profile', 'Skewness of the integrated profile', 'Standard deviation of the DM-SNR curve'. 
        Mean of the DM-SNR curve and Mean of the integrated profile are both found in the features found in Task 5. 
        
#[ ]Task 7: 

#[ ]Task 8: 

#[ ]Task 9(Bonus): 

