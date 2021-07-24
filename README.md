# Problem Statement
Look to  provide a model to find undervalued properties for investment/flipping and assess what factors drive price
 - How well do we predict typical prices?
 - What features dictate the price the most?

# Data Dictionary:

 - 'var_num' is a numberfied version of category, ordered by average sale price for value in category 
|Feature|Type|Description|
|---|---|---|
|MS SubClass|int64| Identifies the type of dwelling involved in the sale |
|MS Zoning|object| Identifies the general zoning classification of the sale |
|Lot Frontage|float64| Linear feet of street connected to property |
|Lot Area|int64| Lot size in square feet |
|Alley|object| Type of alley access to property |
|Lot Shape|object| General shape of property | 
|Land Contour|object| Flatness of the property |
|Utilities|object| Type of utilities available |
|Lot Config|object| Lot configuration |
|Land Slope|object| Slope of property |
|Neighborhood|object| Physical locations within Ames city limits |
|Condition 1|object| Proximity to various conditions |
|Condition 2|object| Proximity to various conditions (if more than one is present) |
|Bldg Type|object| Type of dwelling |
|House Style|object| Style of dwelling |
|Overall Qual|int64| Rates the overall material and finish of the house |
|Overall Cond|int64| Rates the overall condition of the house |
|Year Built|int64| Original construction date |
|Year Remod/Add|int64| Remodel date (same as construction date if no remodeling or additions) |
|Roof Style|object| Type of roof |
|Roof Matl|object| Roof material |
|Exterior 1st|object| Exterior covering on house |
|Exterior 2nd|object| Exterior covering on house (if more than one material) |
|Mas Vnr Type|object| Masonry veneer type |
|Mas Vnr Area|float64| Masonry veneer area in square feet |
|Exter Qual|int64| Evaluates the quality of the material on the exterior |
|Exter Cond|int64| Evaluates the present condition of the material on the exterior |
|Foundation|object| Type of foundation |
|Bsmt Qual|int64| Evaluates the height of the basement |
|Bsmt Cond|int64| Evaluates the general condition of the basement |
|Bsmt Exposure|object| Refers to walkout or garden level walls |
|BsmtFin Type 1|object| Rating of basement finished area |
|BsmtFin SF 1|float64| Type 1 finished square feet |
|BsmtFin Type 2|object| Type 2  Rating of basement finished area (if multiple types) |
|BsmtFin SF 2|float64| Type 2 finished square feet |
|Bsmt Unf SF|float64| Unfinished square feet of basement area |
|Total Bsmt SF|float64| Total square feet of basement area |
|Heating|object| Type of heating |
|Heating QC|object| Heating quality and condition |
|Electrical|object| Electrical system |
|1st Flr SF|int64| First Floor square feet |
|2nd Flr SF|int64| Second floor square feet |
|Low Qual Fin SF|int64| Low quality finished square feet (all floors) |
|Gr Liv Area|int64| Above grade (ground) living area square feet |
|Bsmt Full Bath|float64| Basement full bathrooms |
|Bsmt Half Bath|float64| Basement half bathrooms |
|Full Bath|int64| Full bathrooms above grade |
|Half Bath|int64| Half baths above grade |
|Bedroom AbvGr|int64| Bedrooms above grade (does NOT include basement bedrooms) |
|Kitchen AbvGr|int64| Kitchens above grade |
|Kitchen Qual|int64| Kitchen quality |
|TotRms AbvGrd|int64| Total rooms above grade (does not include bathrooms) |
|Functional|object| Home functionality (Assume typical unless deductions are warranted) |
|Fireplaces|int64| Number of fireplaces |
|Fireplace Qu|int64|  Fireplace quality (ordinal quality) |
|Garage Type|object| Garage location |
|Garage Yr Blt|float64| Year garage was built |
|Garage Finish|object| Interior finish of the garage |
|Garage Cars|float64| Size of garage in car capacity |
|Garage Area|float64| Size of garage in square feet |
|Garage Qual|int64| Garage quality (oridinal) |
|Garage Cond|int64| Garage condition |
|Wood Deck SF|int64| Wood deck area in square feet |
|Open Porch SF|int64| Open porch area in square feet |
|Enclosed Porch|int64| Enclosed porch area in square feet |
|3Ssn Porch|int64| Three season porch area in square feet |
|Screen Porch|int64| Screen porch area in square feet |
|Pool Area|int64| Pool area in square feet |
|Pool QC|int64| Pool quality |
|Fence|object| Fence quality |
|Misc Feature|object| |
|Misc Val|int64| Miscellaneous feature not covered in other categories |
|Mo Sold|int64| Month Sold (MM) |
|Yr Sold|int64| Year Sold (YYYY) |
|Sale Type|object| Type of sale |
|SalePrice|int64| Sale Price $ |
|total_sf|float64| total square feet of house |
|baths|float64| total number of baths + half baths |
|has_porch|int32| has a porch |
|porch_sf|int64| total porch square footage |
|sold_after_0601|int64| months after Jan 2006 it was sold |
|blt_after_1900|int64| Build date relative to 1900 |
|rem_after_1900|int64| Remodel date relative to 1900 |
|has_basement|int32| has a basement |
|neigh_num|int64| Neighborhood number ordered by avg saleprice |
|ms_num|int64| MS Subclass numberfied (See Above) |
|zone_num|int64| MS Zone numberfied |
|lotshape_num|int64| lot shape numberfied (See Above) |
|landcont_num|int64| land contour numberfied (See Above) |
|util_num|int64| Utilities numberfied (See Above) |
|lotconf_num|int64| Lot Configuration numberfied (See Above) |
|slope_num|int64| Lot Slope numberfied (See Above) |
|cond1_num|int64| Lot Condition 1 numberfied (See Above) |
|cond2_num|int64| Lot Condition 2 numberfied (See Above) |
|bldgtyp_num|int64| Home Building type numberfied (See Above) |
|houstyle_num|int64| Style of House numberfied (See Above) |
|roofst_num|int64| Roof Style numberfied (See Above) |
|roofmat_num|int64| Roof Material numberfied (See Above) |
|ext1_num|int64| Primary exterior finish numberfied (See Above) |
|ext2_num|int64| Secondary exterior finish numberfied numberfied (See Above) |
|masvnrtyp_num|int64| Masonry veneer type numberfied (See Above) |
|found_num|int64| Foundation type numberfied (See Above) |
|bsmtexp_num|int64| Basement Exposure numberfied (See Above) |
|bsmtfin1_num|int64| Basement Finish 1 numberfied (See Above) |
|bsmtfin2_num|int64| Basement Finish 2 numberfied (See Above) |
|heat_num|int64| Heating numberfied numberfied (See Above) |
|elec_num|int64| Electricity numberfied (See Above) |
|gartyp_num|int64| Garage Type numberfied (See Above) |
|fence_num|int64| Fence type numberfied numberfied (See Above) |
|garfin_num|int64| Garage Finish numberfied (See Above) |
|func_num|int64| Home Functionality numberfied (See Above) |
|misc_num|int64| Miscelaneous features  numberfied (See Above) |
|sale_num|int64| Type of sale numberfied (See Above) |
|Street_Pave|uint8| Street is Paved (1 Y/ 0 N) |
|Central Air_Y|uint8| Has Central air (1 Y/ 0 N) |
|Paved Drive_P|uint8| Has Partial Paved Drive (1 Y/ 0 N)  |
|Paved Drive_Y|uint8| Has Paved Drive (1 Y/ 0 N)|

Terms with `value1*value2` are the above terms number values multiplied together. 

# Brief analysis

Looking at the correlation matrix, many of the normal factors one would expect hafve the larges effect on the sale price of a house, namely quality, which neighborhood, how big features are, etc. 

Not many of the provided information is negatively correlated by itself to the sale price, and some of them are counter intuitive, for example the worst correlation is between the number of above ground kitchens to the sale price. This is probably driven by lack of statistics for houses with 4 kitchens or underlying factors in that case. 

As would be expected, there traits you normally hear people wanting in a house (big, good qualtiy, big lot, etc) are more strongly correlated with the price. 

Looking at the scatter plots, there seem to be a couple outliers for a few of the single distributions for continuous data. Namely, there are a couple instances in total square footage, that are greatly separated from everything else, probably indicating some relation not show in just those plots, or missing information. When the numberized neighborhood is included into things, those are brought back into line, but then a few more, not so drastic outliers emerge. As much as overfitting isn't desired, there is also a good bit of nuance that might not be able to be expressed by the data no matter how hard is tried. 

Interaction terms are introduced in order to boost the power of the potential fit. This greatly increases the phase space for potential fits, but also dilutes a bit of the conclusion power as a bit of it is throwing things at the wall and seeing what sticks. Looking for continued tendencies in represented variables shows the power of things related to size, condition, and other things, while also showing some of the loss of inference in things like `MS Subclass` showing up as one of the fit parameters, and earlier than something like fireplaces by itself. 

The fit itself was limited to 40 variables in order to stay somewhat close to the metric of limiting the number of parameters to $\sim\sqrt(N)$ where N is the total number of entries being fit to. I decided to fit how I did because of a limitation in computing power. If one would want to find the best 40 term pair, they would allow for all combinations of 40 paramaters from the 1856 available to be tested and look for the best result. The issue with this is in this case that would mean $\sim4/cdot10^{82}$ different combinations would need to be tested. To avoid this, I worked to just do iterations one at a time, where the computation limitation would be relative to `N*K` where N is the number of potential parameters and K is the number of fit parameters. The fit could be extended to allow further interaction terms or terms of higher order, but this will also increase runtime significantly. 

The resulting fit was decided useing a `cross_val_score` with a `cv = 5` to minize the mean squared error. Each iteration would choose one new value, and would be one of the parameters included in the next fit. For example `'total_sf*neigh_num'` is the first selection, and the second iteration looks for the best fit using `'total_sf*neigh_num'` and a new variable. Because many variables are correlated to each other, especially in addition to the cross terms, the goal is that at the number of variables, enough of the variance is covered even though it may not be the optimal available. 

The overlap between variables is seen when doing it this way. Two of the strongest variables, `'total_sf*neigh_num'` and `'Overall Qual*total_sf'` are strongly correlated to each other, and when the fit chooses one, the other is not found until much later in the process. 

Overall my fit with the training data is found to have the following test statistics:

|$R^2$ Train| $R^2$ Test | RSME |
|---|---|---|
| 93.643% | 93.803% | $20306 |

This fit seems to be performing well, and it seems to have good predictive power. When submitted to Kaggle, it also seems to do well, although the RMSE is on the edge of what is expected from the standard deviation from the cv fit. 

Ridge and Lasso were also attempted with all of the available parameters, but they do not seem to perform as well with more parameters used compared to the standard LR fit, so the standard LR fit was used. 

Most of the output parameters were interaction terms, which loses a bit of the straight interpretation. But repeated terms can be useful, and looking at terms that may be complementary. 

# Conclusion

The fit performs fairly well and seems to be able to predict outcomes well. We can explain more than 93% of the variability of the data with our fit, and the RMSE is closing in on 20k, which is a rough evaluator for far off we expect any prediction. The mean absolute error is around 14k, which is the true average value for how far off any guess would be. 

I can conclude that we can successfully predict house value with my model, and the recurring themes within it show what consumers value most when buying homes. Some are more obvious in the size dirving prices, but the weight of other features, such as kithcen quality, show the potential for significanlty raising house value with targeted changes. 

Ultimately, this is a model and there are points, especially for outliers, that may not be accounted for. It should be used as a guide, with further due diligence to shore up outstanding uncertainties. 