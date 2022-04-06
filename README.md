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

  ![image](https://user-images.githubusercontent.com/94253815/161868565-57837af5-b718-4a2f-a6d2-ddccd3b1b5f2.png)


  ![image](https://user-images.githubusercontent.com/94253815/161868810-ad245c7c-e047-4a05-965c-f89cbc05402a.png)


 * Compiling, Training, and Evaluating the Model

   * How many neurons, layers, and activation functions did you select for your neural network model, and why?
   ![image](https://user-images.githubusercontent.com/94253815/161868997-3921da17-f2d1-4fd3-8216-5944d477ff67.png)
   * 80 Neurons used for the 1st layer
   * 2nd hidden layer - 30 layers chosen - wanted to achieve additional processing without overfitting.
   * In both layers, "relu" activation function was was used and on the final output, "sigmoid" function was used.
   
   * Were you able to achieve the target model performance?
   * I was not able to hit the target performance on the 1st go around.
   * Loss - 55.47%
   * Accuracy -72.52%
   
   ![image](https://user-images.githubusercontent.com/94253815/161869758-7aaf5550-ab18-437e-ad6e-1ef234fa1cef.png)

  ##Optimization Test
   * 1st go around did not give us th resluts we were looking for. Some changes were done to see if we could improve proformance.

   * Optimization 1 
   ![image](https://user-images.githubusercontent.com/94253815/161870078-b1c49782-8b46-41ae-8def-133a34e2a11c.png)

   * Optimization 2
   
   

## Summary
