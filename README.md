# Neural_Network_Charity_Analysis

## Overview of the Analysis
  The purpose of this analysis was to employ deep learning models in order to aid a fictitious company named AlphabetSoup.  By training a deep learning model on a retrospective dataset of about 30,000 historical donations for both successful and unsuccessful outcomes, the model served as a binary classifier to predict whether applicants would be successful if given funding. In summary, this would help Alphabet Soup know where to place their funds.
The deep learning model performed supervised learning by training on the "feature" columns from the dataset to predict a "target" column containing binary values of "0" or "1", as these numbers were indicative of whether the donation of each observation produced an unsuccessful or successful outcome.  To maximize the performance and prepare it for the neural network model, the data required significant preprocessing. Following this, the data was compliled, trained, and the results were evaluated. The details and results of this process are described further below.
 

## Results

 * Data Preprocessing
    * To begin, the dat was inspected and analyzed.
    * "EIN and "NAME" were dropped due to being deemed unuseful.
    
 ![image](https://user-images.githubusercontent.com/94253815/161866882-6bae8562-bc2c-467a-bb31-927c0ebf2bd1.png)

 

   * What variables are considered targets for your model?
   * "IS_SUCCESSFUL" column
  
  ![image](https://user-images.githubusercontent.com/94253815/161867070-1b915e96-ef98-403e-b92c-e02a0b7b866e.png)


   * What variable are considered to be features for your model?
      * APPLICATION_TYPE—Alphabet Soup application type
      * AFFILIATION—Affiliated sector of industry
      *  CLASSIFICATION—Government organization classification
      *  USE_CASE—Use case for funding
      *  ORGANIZATION—Organization type
      *  STATUS—Active status
      *  INCOME_AMT—Income classification
      *  SPECIAL_CONSIDERATIONS—Special consideration for application
      *  ASK_AMT—Funding amount requested


   * The number of unique values from each column was calculated using the nunique() method from the pandas library.
   
   ![image](https://user-images.githubusercontent.com/94253815/161868406-9f2d3033-19e4-4a89-b229-a2f2edebeaf6.png)

   
   * This allowed us to visualize which columns had more than 10 unique values and, thus, would need bucketing into an "other" column to reduce the number of dummy columns that would result when converting categorical variables to numerical format later. 
   * Two categorical variables, "APPLICATION_TYPE" and "CLASSIFICATION" fell into this category. "ASK_AMT" was a numerical column and thus did not need attention.

 * Compiling, Training, and Evaluating the Model

   * How many neurons, layers, and activation functions did you select for your neural network model, and why?
   * Were you able to achieve the target model performance?
   * What steps did you take to try and increase model performance?

## Summary
