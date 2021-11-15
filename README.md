# GHG EMISSION IN THE UK
Forcasting for the next 5 years - A Time series Analysis with FbProphet

### Dataset

The GHG emissions in the Uk dataset from ONS atmospheric emissions was selected. The dataset contained several sheets of the different GHG emissions in the UK over the period of 1990 - 2020.
However, for this model we used the first sheet from the dataset which contained the total GHG emissions from all sectors from 1990 - 2020.

Data source 
https://www.ons.gov.uk/economy/environmentalaccounts/datasets/ukenvironmentalaccountsatmosphericemissionsgreenhousegasemissionsbyeconomicsectorandgasunitedkingdom

### Preprocessing and Cleaning

The dataset was loaded into a pandas dataframe. The row in the table containing the years in the dataset was promoted and made the header of the table, the rows containing null value was dropped, as well as the columns containing null values.

The columns were renamed and missing values were checked and removed from the table, and the data was sliced by its index containing the roles I was interested in. Howeve, I was working with the row containing the Total GHG emmissions value, which was sliced out of the table.

The new table containg the total GHG emissions was unpivoted and re-indexed, the columns were renamed and the data type for the columns were changed to suit the modelling of the data.

The columns were renamed into 'ds' for the year column and 'y' for the GHG emissions value column.

### Training Model and Forecasting

The fbprophet library was utilised for this time series analysis in forecasting GHG emissions in the UK for the next 5years.  
The model was instantiated with a 95% confidence interval. The model was trained with the preprocessed data and used to make prediction for a period of 5 years. 

### Result

The figure above has shown a great decrease in the total GHG emissions in the UK from 1990 - 2020. 

The forecast for the next 5 years has shown that the GHG emissions would continue to decrease significantly over the next five years as seen in the trend of the projection. 

### Implication to UK Government

Given the targeted net zero GHG emissions by 2050, this forecast has shown a 50% reduction of GHG emissions from 1990 to 2025,  with the aim targetting 80% reduction in GHG emissions compared with the levels of 1990, 
adequate measures needs to be taken to achieve this goal. 
Further research needs to carried out to check which particular industries is increasingly contributing to this GHG emissions and look at measure to futher remove and reduce the GHG emissions. 


## FORECASTING FOR THE NEXT 5 YEARS WITH POWERBI

### RESULT FROM POWERBI

 FIG 1. Forecast of GHG Emissions for the next Five Years

![forecast](https://user-images.githubusercontent.com/63594833/141844817-66936b0d-9fdb-4868-8330-61e223327610.PNG)

 
