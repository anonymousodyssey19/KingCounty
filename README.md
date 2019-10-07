# King County Project Overview:

I have been hired by a Real Estate Investing company to look into the real estate data of King County, in which they operate, and provide them with a data driven strategy. Specifically, I am to provide 1 "main focus" and two actionable steps that align with the "main focus" so that they are able to achieve the highest ROI when they invest.

## Final Model Results:

R2-Value: 0.85

P-Value: 0.00

Predictors: Sqft (Living), Zipcode, Bedrooms, Building Grade

Model: OLS (Code Provided)

       

# Summary

## PROCESS:
           

### Obtain:

I started by getting the understanding of what the Real Estate Investing company wanted from me. While they were not specific questions, they were questions that could be answered with the dataset that was given to me. I loaded the CSV file twice in this notebook; Once to get the dataframe to create my model, and the second to provide the "real" numbers that are more easily digestable for the non technical crowd.

### Scrub/Explore:

During this stage I initially focused on the scrubbing element of the OSEMN process by figuring out which columns had NaN values and dealing with those on a case by case value that is listed above. From there, in a combination of the two steps I then went to through and updated columns as needed. Whether they needed to change the category or be removed, all steps are listed above. This allowed me to create a reliable model and required a few passes over to get right.

### Model:

In modelling the data I had to made sure to run a few different models. Whether I changed the normalization of the independent variable or ran the model after one hot encoding certain columns. After, I made sure to test the model to ensure that I could add multiple predictors and it would hold up.

### Interpret:

This was actually the most fun part for me. I have an interest in real estate investing so, what this data allowed me to see about the real estate in this county quickly turned into me nerding out and often times biting off more than I could chew. It did push me to create visualizations that were a little beyond my skillset at the start of this project because I knew that, given my experience, the would be relevant in this industry.


## MODEL:

I used two models due to having both numerical data as well as categorical data. For the categorical model I one hot encoded all the categorical data. The grade column's r-value held up after one hot encoding and actually ended up in the top three for highest r-values. This answers WHAT their main focus should be although it is a vague predictor, the website that explains each "grade" says that their is a direct relationship with one of the other three highest predictors: "sqft_living". "Zipcodes" signifigantly increased their r-value after being one hot encoded to create the highest r-value. This answers WHERE they should focus in order to achieve their main focus and is why I chose it as a predictor. The other model was used to calculate the numerical data. I made sure to normalize price column with another model to ensure that it was not effecting the results. I took the predictor that had the highest r-value. I was also going to take the "grade" column from this model but needed to make sure that because it was categorical data that the r-value held up even after it was one hot encoded. The predictor that had the third highest r-value was the "sqft_living" column. This answers HOW they should be achieving their main focus as a company and is why I used it as a predictor. The last predictor that I used was "bedrooms". It does not have the highest r-value but given my knowledge of the industry, I know that it is a very tangible and actionable aspect when redeveloping real estate. I targetted the highest increase in coeffecient between bedrooms while also taking into account the amount of homes that fall in that specific category of bedrooms when determining my recomendations.
