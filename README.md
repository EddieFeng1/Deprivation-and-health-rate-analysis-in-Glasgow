# Deprivation-and-health-rate-analysis-in-Glasgow
## Introduction
This exploration based on Index of Multiple Deprivation (IMD) and the Scottish census in 2011 to explore the correlations and relationships between those two varibles in Glasgow. Quantify two variables using a graph and explore their correlation. The spatial regression model explores the spatial relationship between two variables and uses MSE to judge the accuracy of the model. Finally, the accurate model output is presented in the form of a map.

## Progress of good health rate and deprivation analysis in Glasgow
### Step 1. Data Collection
The objective of this research endeavor is to comprehensively analyze and elucidate the interplay and associations between the Index of Multiple Deprivation (IMD) and demographic data derived from the 2011 Scottish census within the context of Glasgow, thereby providing a nuanced understanding of socio-economic dynamics within the region. And the areas based on the data zone in 2011, which confirm the all data have the regional diviation.



### Step 2. Data Cleaning
The study focuses on selecting specific areas within Glasgow from the multitude of data zones recorded in the 2011 Scottish census. This meticulous selection process ensures a targeted examination of socio-economic characteristics within Glasgow's diverse neighborhoods, facilitating a more precise analysis of the correlations between the Index of Multiple Deprivation (IMD) and demographic factors.

And using box plot and scatter plot to check for the outliers and trends, which found several outliers in the dataset and the greater good health rate in the rich areas.

### Step 3. Spatical Regression Analysis
Using spatical regression analysis to explore the spatial autocorrelation between good health rates and deprivation indices using spatial regression analysis.

In this spatial regression analysis, we use Maximum Likelihood Estimation (MLE) model, whcih could "estimate the larameters of an assumed proability distribution, given observd data" (Wiki, 2024) and Queen method to build the martix, which could confime the spatial weights. Queen's method (or King's) is a most commom way to build the spatial weights matrix, particularly, Queen's Method has less nonezero elements because of the definition of neighbourhood (Ijumulana et al, 2020, pp.139584). So that, the Queen's is suitable for this case.

First of all, the strong and positive correlation, 0.83, between two variables proved the features can apply MLE model.

Then, The health rate was then used as the independent variable and the deprivation index as the dependent variable respectively in the model. Then use deprivation as the independent variable and health rate as the dependent variable, and apply the model again.

### Step 4. Check the results of models
Using Mean Square Error (MSE) to check the predicted values wether accurate to judge the accurate of the model. The model exlpores how much good health rate affects deprivation index shows 2.42 MSE, which is too great for the original values. As the result, the model should be further discussed and developed. The model taht researches the effect on deprivation for health rate shows 0.00295 MSE, which fair enough to prove the accurate of the model.

When deprivation is treated as the independent variable and health rate as the dependent variable, it aligns with our intuitive understanding of how socioeconomic factors (deprivation) can influence health outcomes (health rate). In contrast, the reversed setup where health rate is treated as the independent variable and deprivation as the dependent variable might not make as much sense in this context. It's less intuitive to think of health rate causing deprivation. While there may be some bidirectional causality or feedback loops between health and socioeconomic status, in most cases, socioeconomic factors are considered to be the driving force influencing health outcomes.

### Step 5. Visulization
Select the predicted values of the model which explores how much deprivation affects health rate. And map those data on the map of Glasgow.

The area in the northernmost area has the higher 'very good health rate'. Most zones surronding it in the northern Glasgow generally have the lower good health rate. In the western Glasgow, upon the Rive Clyde, most zones have the unfavorable ratios, except some area at in the eastern most corners, which have higher good health situation. In the west of Glasgow, upon Clyde River, some areas have the better situation. But many discts in the western most corner have bad situation in health.

Below the River Clyder, many residents in the eastern districts don't have very good health rate. The people live in the west zones below River Clyder a little better than people in the west below the river, but still have the lower health situation. The citizen in the centre of the southern Glasgow (below the River Clyder) have higher health situation.

# Reference
Wikipedia. 2024. Maximum likelihood estimation. [Online]. [Accessed 12 April 2024]. Available from: [https://en.wikipedia.org/w/index.php?title=Maximum_likelihood_estimation&action=history]

Ijumulana, J., Ligate, F., Bhattacharya, P., Mtalo, F. and Zhang, C. 2020. Spatial analysis and GIS mapping of regional hotspots and potential health risk of fluoride concentrations in groundwater of northern Tanzania. The Science of the total environment. 735, pp.139584–139584.

