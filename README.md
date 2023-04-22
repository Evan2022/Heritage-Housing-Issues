## Dataset Content
* The dataset is sourced from [Kaggle](https://www.kaggle.com/codeinstitute/housing-prices-data). We then created a fictitious user story where predictive analytics can be applied in a real project in the workplace. 
* The dataset has almost 1.5 thousand rows and represents housing records from Ames, Iowa, indicating house profile (Floor Area, Basement, Garage, Kitchen, Lot, Porch, Wood Deck, Year Built) and its respective sale price for houses built between 1872 and 2010.

|Variable|Meaning|Units|
|:----|:----|:----|
|1stFlrSF|First Floor square feet|334 - 4692|
|2ndFlrSF|Second-floor square feet|0 - 2065|
|BedroomAbvGr|Bedrooms above grade (does NOT include basement bedrooms)|0 - 8|
|BsmtExposure|Refers to walkout or garden level walls|Gd: Good Exposure; Av: Average Exposure; Mn: Minimum Exposure; No: No Exposure; None: No Basement|
|BsmtFinType1|Rating of basement finished area|GLQ: Good Living Quarters; ALQ: Average Living Quarters; BLQ: Below Average Living Quarters; Rec: Average Rec Room; LwQ: Low Quality; Unf: Unfinshed; None: No Basement|
|BsmtFinSF1|Type 1 finished square feet|0 - 5644|
|BsmtUnfSF|Unfinished square feet of basement area|0 - 2336|
|TotalBsmtSF|Total square feet of basement area|0 - 6110|
|GarageArea|Size of garage in square feet|0 - 1418|
|GarageFinish|Interior finish of the garage|Fin: Finished; RFn: Rough Finished; Unf: Unfinished; None: No Garage|
|GarageYrBlt|Year garage was built|1900 - 2010|
|GrLivArea|Above grade (ground) living area square feet|334 - 5642|
|KitchenQual|Kitchen quality|Ex: Excellent; Gd: Good; TA: Typical/Average; Fa: Fair; Po: Poor|
|LotArea| Lot size in square feet|1300 - 215245|
|LotFrontage| Linear feet of street connected to property|21 - 313|
|MasVnrArea|Masonry veneer area in square feet|0 - 1600|
|EnclosedPorch|Enclosed porch area in square feet|0 - 286|
|OpenPorchSF|Open porch area in square feet|0 - 547|
|OverallCond|Rates the overall condition of the house|10: Very Excellent; 9: Excellent; 8: Very Good; 7: Good; 6: Above Average; 5: Average; 4: Below Average; 3: Fair; 2: Poor; 1: Very Poor|
|OverallQual|Rates the overall material and finish of the house|10: Very Excellent; 9: Excellent; 8: Very Good; 7: Good; 6: Above Average; 5: Average; 4: Below Average; 3: Fair; 2: Poor; 1: Very Poor|
|WoodDeckSF|Wood deck area in square feet|0 - 736|
|YearBuilt|Original construction date|1872 - 2010|
|YearRemodAdd|Remodel date (same as construction date if no remodelling or additions)|1950 - 2010|
|SalePrice|Sale Price|34900 - 755000|





## Business Requirements
As a good friend, you are requested by your friend, who has received an inheritance from a deceased great-grandfather located in Ames, Iowa, to  help in maximising the sales price for the inherited properties.

Although your friend has an excellent understanding of property prices in her own state and residential area, she fears that basing her estimates for property worth on her current knowledge might lead to inaccurate appraisals. What makes a house desirable and valuable where she comes from might not be the same in Ames, Iowa. She found a public dataset with house prices for Ames, Iowa, and will provide you with that.

* 1 - The client is interested in discovering how the house attributes correlate with the sale price. Therefore, the client expects data visualisations of the correlated variables against the sale price to show that.
* 2 - The client is interested in predicting the house sale price from her four inherited houses and any other house in Ames, Iowa.


## Hypothesis and how to validate?
* 1 - The size of the house in terms of square footage is positively correlated with the sale price. 
    * Validation: We can create a scatter plot to visualize the relationship between the size of the house and the sale price. if the plot shows a clear trendline sloping upwards, we can conclude that there is positive correlation between the two variables. 

* 2 - The age of the house is negatively correated with the sale price. 
    * Validation: We can create a scatter plot to visualize the relationship between the age of the house and the sale price. If the plot shows a clear trendline sloping downwards, we can conclude that there is a negative correlation between the two variables. 

* 3 - The presence of a garage is positively correlated with the sale price. 
    * Validation: We can create a bar chart to compare the average sale price of houses with and without garages. If the chart shows that houses with garages have a higher average sale price, we can conclude that there is a positive correlation between the presence of a garage and the sale price. 

* 4 - The overall quality of the house is positively correlated with the sale price. 
    * Validation: We can create a box plot to compare the distribution of sale prices for houses with different overall quality ratings. if the plot shows that houses ith higher overall quality ratings tend to have higher sale prices, we can conclude that there is a positive correlation between the two variables.


## The rationale to map the business requirements to the Data Visualisations and ML tasks
* 1 - Business requirement 1 - To meet the first business requirement, we need to preform exploratory data analysis (EDA) on the dataset and create visualizations that can help us understand the relationship between different house attributes and the sale price. We can use scatter plots, box plots, bar charts, and other types of visualizations to identify correlations between variables. We can use tools such as matplotlib, seaborn and pandas for data visualization.

* 2 - Business requirement 2 - To meet the second business requirement, we need to use machine learning algorithms to train a model that can predict the sale price of a house based on its attributes. We can use regression algorithms such as linear regression, decision tree regression, or random forest regression to build a predictive model. We need to select appropriate features, cleaning and preprocessing the data, splitting it into training, test and validation sets and evaluating the preformance of the model.


## ML Business Case
* 1 - What are the business objectives? 
    * The business objective of this project is to help the client maximize the sales price for their inherited properties in Ames, Iowa by building a machine learning model that can accurately predict the sale price of houses based on their attributes.

* 2 - Is there any business objectives that can be answered with conventional data analysis? 
    * Conventional data analysis could help the client understand the relationship between the different attributes of the houses and the sale price, but it would not be able to accurately predict the sale price of a given house.

* 3 - Does the client need a dashboard or and API endpoint? 
    * Dashboard in this case. 

* 4 - What does the client consider as a successful project outcome? 
    * The client considers the project a success if the machine learning model can accurately predict the sale price of houses in Ames, Iowa with a high degree of accuracy.

* 5 - Can you break down the project into Epics and User stories?
    * Yes, please see Epics and User Stories section: 

* 6 - Ethical or privacy concerns?
    * No, this dataset is public sourced from Kaggle and does not contain any sensitive information about the properties or the homeowners. 

* 7 - Does he data suggest a paticular model? 
    * Based on the size of the dataset and the nature of the problem, a regression model would be a suitable choice for this project. Specifically, a linear regression or a decision tree regression model could be used.

* 8 - What are the models inputs and intended outputs? 
    * The model inputs would be the different attributes of the houses, such as the size, age, number of bedrooms, number of bathrooms, presence of a garage, and overall quality rating. The model output would be the predicted sale price of the house.

* 9 - What are the criteria for the performance goal of the predictions? 
    * The performance of the model will be evaluated using metrics such as mean absolute error, mean squared error, and R-squared. The goal is to minimize the error and maximize the R-squared value to ensure the model is accurately predicting the sale price.

* 10 - How will the client benefit?
    * The client will benefit from this project by being able to accurately predict the sale price of their inherited properties and any other house in Ames, Iowa. This will help them make more informed decisions about pricing and marketing their properties, ultimately maximizing their sale price and profitability.


## Dashboard Design
* List all dashboard pages and their content, either blocks of information or widgets, like buttons, checkboxes, images, or any other items that your dashboard library supports.
* Eventually, during the project development, you may revisit your dashboard plan to update a given feature (for example, at the beginning of the project you were confident you would use a given plot to display an insight but eventually you needed to use another plot type)



## Unfixed Bugs
* You will need to mention unfixed bugs and why they were not fixed. This section should include shortcomings of the frameworks or technologies used. Although time can be a big variable to consider, paucity of time and difficulty understanding implementation is not valid reason to leave bugs unfixed.

## Deployment
### Heroku

* The App live link is: https://YOUR_APP_NAME.herokuapp.com/ 
* Set the runtime.txt Python version to a [Heroku-20](https://devcenter.heroku.com/articles/python-support#supported-runtimes) stack currently supported version.
* The project was deployed to Heroku using the following steps.

1. Log in to Heroku and create an App
2. At the Deploy tab, select GitHub as the deployment method.
3. Select your repository name and click Search. Once it is found, click Connect.
4. Select the branch you want to deploy, then click Deploy Branch.
5. The deployment process should happen smoothly if all deployment files are fully functional. Click the button Open App on the top of the page to access your App.
6. If the slug size is too large then add large files not required for the app to the .slugignore file.

## Main Data Analysis and Machine Learning Libraries
* Here you should list the libraries you used in the project and provide example(s) of how you used these libraries.


## Credits 

* In this section, you need to reference where you got your content, media and extra help from. It is common practice to use code from other repositories and tutorials, however, it is important to be very specific about these sources to avoid plagiarism. 
* You can break the credits section up into Content and Media, depending on what you have included in your project. 

### Content 

- The text for the Home page was taken from Wikipedia Article A
- Instructions on how to implement form validation on the Sign-Up page was taken from [Specific YouTube Tutorial](https://www.youtube.com/)
- The icons in the footer were taken from [Font Awesome](https://fontawesome.com/)

### Media

- The photos used on the home and sign-up page are from This Open Source site
- The images used for the gallery page were taken from this other open-source site



## Acknowledgements (optional)
* In case you would like to thank the people that provided support through this project.

