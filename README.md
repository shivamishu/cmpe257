# cmpe257 Midterm
Machine Learning IOWA Housing Dataset problem

# Fall 2021 Midterm Project
## ***IOWA Housing Dataset Scrapping Additional Dataset/Enrichment***
### Shivam Shrivastav
### SJSU ID: 015275000

Main Dataset Link: https://drive.google.com/drive/u/4/folders/1o8xOlyoERxwW1j60WHRp7yLflHcC2O3A  
IOWA Dataset Link: https://drive.google.com/file/d/1h6jeu_81VLLa3qXSyzmlUw_ub6ia8Q2E/view?usp=sharing    
Scrapped Dataset: https://drive.google.com/file/d/1pFhkGNJbM1Eah3qxyZDZvUTUprYXf_Va/view?usp=sharing   

**Business Case**
 * Provide knowledge to an investor or buyers, whether to invest in a housing porperty or not.   
 * This decison has to be taken by considering various features such as, Selling Price of the property, Zestimate Price, Proximity Ranking to various Schools, Crime Rate in the area, Walk Score etc.

1) Data narrative: Using IOWA Dataset given by the professor, I 
rmed Data cleaning, data preparation and eliminated unwanted columns and considered only the required features such as, address, zipcode, area, bedrooms, bathrooms, year built, price, zesitmate, zestimate rent.
Apart from this data, I scrapped serveral addtional dataset from above mentioned websites to enrich the intial dataset, amalgamate it and improve the feature set and visualization of deduce the best model.

2) ***Visualizations:***  
- Performed Visualizations of data preparation using First, Second and Third Data Enrichment.

- Calculated Feature importance, gini score.

2) **Web Scraping**: I scrapped serveral addtional dataset from above mentioned websites to enrich the intial dataset, amalgamate it and improve the feature set and visualization of deduce the best model.  
Final Scrapped Dataset file store in drive is 'shivam_final_scrapped_data.csv'.  

Zillow: https://www.zillow.com  
Walk Score: https://www.walkscore.com   
School Proximity Rank: https://www.niche.com/places-to-live/z/  
Crime rates: https://247wallst.com/city/  

3) ***Data Preparaion***    
Peformed Feature transformation: Transform features  and add new features to dataset via amalgamations   


4) ***Data Distribution*** Did Dimensionality Reduction via PCA      
 - Implement 3 amalgamations:    
First dataset Enrichment     
Second data Enrichment    
Third data enrichment

5.) Performed the ***First, Second and Third Data Enrichment*** by mering Zellow data, Walk Score Data, School Rank Data and Crime rates data into the Housing dataset in DataFrame itself.
Link to Scrapped Dataset:  https://drive.google.com/file/d/1pFhkGNJbM1Eah3qxyZDZvUTUprYXf_Va/view?usp=sharing   
IOWA Dataset Link: https://drive.google.com/file/d/1h6jeu_81VLLa3qXSyzmlUw_ub6ia8Q2E/view?usp=sharing     

6) **Feature Transformation**: Cleaned the final dataset and scrapped dataset, performed feature transformation by checking null values, lable encoding, and store in dataframe for further processing. 

7) **Feature Importance**: With the help of Correlation Coefficient Heatmap and gini score, I deduced House price, Mortgage+HOA, Zestimate Price, area, zestimate rent, zipcode, crime rate, school proximity rank and, WalkScore as the most important features from the final dataset.

8) **Clustering** : Used ScikitLearn K-Means clustring for the dataset. To observe the dataset, Created clusters for the various feature combinations. Below mentioned are my observations:

9) ***Observations from above***
- ***Rent and HOA+Mortgage Fees***: Profit on House rent deducting the HOA + Mortgage fees seems to be a good factor on deciding the profitable investment scope. Houses with more rent and low HOA+Mortgage Fees tend to have high price but high profit.   
- ***House Price and zipcode***: Zipcodes have various properties ranging from lowest to highest price.
- ***zestimate rent and zestimate price***: Properties having less zestimate price have the low rent and properties having the high zestimate price have high rent.
- ***School Proximity Rank as Zestimate price***: Properties with high nearby Schools ranking have high property prices and properties nearby schools with low rank have less prices. 
- ***Crime rate and Zestimate price***: Properties in areas with Higher crime rates have the lower zestimate price and properties in areas with lower crime rate have the lower zestimate price. 

10) **Linear Regression**: To predict the actual and predicted average house prices for the house, trained and split the final data set(80:20) with the important features and then first performed Linear regression seprartely to predict the house price. This was done by trainning the model based on the final housing dataset. 

11) **Fractal Clustering**: To suggest a suitale property for an investor to invest on or not, I performed Fractal Clutering on various feature combinations

- ***Rent vs Mortgage+HOA***: The cluster 2 is the goldern cluster where Rent is greater Mortage price and HOA having the difference in the best price range.
- ***House Price and Best School Proximity Rank***: The cluster 0 is the golden cluster where property price is lower and school proximity rank is highest. Most of the houses have 2 or more bedrroms and bath, suitable for a family with kids.
- ***Zestimate price and maximum Walk Score***: Found the cluster 1 as the golden cluster having the maximum walk score for the moderate price.
- ***Zestimate price and crime Score***: Found the cluster 1 as the golden cluster having the lowest crime rate and lower housing prices that would interest the invester to a property.

12) **Latent Variables**: Deduced Walk Ccore, Crime Rate and School Rank, Profit = Rent - (Mortgage+HOA fees)  as the latent variables.

13) **Logistic Regression** : A good investment properties have a positive rental income every month after deducting (Mortgage+HOA fees). Thus, I performed Logistic Regression and created a new feature in the final datafram as 'Invest_or_Not' based on the value where Rent > Mortgage + HOA, which means we get a profit in our rent is much greater than (Mortgage+HOA fees). After training and predicting the model, I got the accuracy of 98%.
Thus, it means most of the properties avialbale in provided IOWA dataset is ideal for an investor to make an investment.

14) **Muller Loop**: I performed Muller Loop to get the best Classifier and Regressor among below to get the best accuracy of the model to help find the properties to invest on.   
***Classifier:***  
"Nearest Neighbors",  
"Linear SVM",  
"RBF SVM",  
"Decision Tree",  
"Random Forest",  
"Neural Net",  
"AdaBoost",  
"Naive Bayes",  
"QDA"  

***Regression:***
"GradientBoostingRegressor",  
"RandomForestRegressor",  
"LinearRegression",  
"SVR",  
"DecisionTreeRegressor",  
"AdaBoostRegressor",  
"GaussianProcessRegressor",   
"LogisticRegressor"  


I found that the accuracy score for the algorithms fluctuate ranging from 90% to 98%. The more I trained the model, the accuracy was getting increased sharply.   

15) ***Pickle and Load*** Prepared a model to load the best model for future reference. 
Link best model:  

16) Build Confusion Matrix and checked Variance in prediction quality 
