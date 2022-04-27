# Challenge-6


## Proptech 

I am an analyst at a Proptech company that wants to offer an instant, one-click service for people to buy properties and then rent them. The company wants to have a trial of this offering in the San Francisco real-estate market. If the service proves popular, we can then expand to other markets.

I will use data visualization skills, including aggregation, interactive visualizations, and geospatial analysis, to find properties in the San Francisco market that are viable investment opportunities.


---

## Technologies

This project leverages Pandas and hvplot on Jupyter notebook

---

## Open Guide

Before running the application first open Jupyter lab in terminal:

```
  1. Activate dev environment by: "conda activate dev"
  2. Open Jupyter Notebook by: "Jupyter lab"
```


---

## Usage

To use the analysis simply clone the repository and run the **san_francisco_housing.ipynb** within the Jupyter Notebook.\
*Import the following libraries and dependencies:*

``` python
import pandas as pd
import hvplot.pandas
from pathlib import Path
```

---

## Calculate and Plot the Housing Units per Year 

1. Use *groupby* function to group the data by year and aggregate the results by the *mean* of the groups.
2. Use *hvplot* function to plot the **Housing Units in San Francisco from 2010 to 2016**. 

![<bar>](<Image/bokeh_plot.png>)

*In this trend, it shows the overall housing units is increasing.*

---


## Calculate and Plot the Average Sale Prices per Square Foot

1. *groupby* the data by year and aggregate the results by the *mean* of the groups.

*The lowest gross rent reported is $1239 on 2010.*

2. Drop **housing_units** column to show only the **sale_price_sqr_foot** and **gross_rent** throughout the period. 
3. Use *hvplot* function to plot the **Sale Price Per Square Foot and Average Gross Rent from 2010 to 2016**.

![<2>](<Image/bokeh_plot (1).png>)

*On 2011, there's a drop in the average sale price per square foot compared to 2010. However, the gross rent is still going up.*

---

## Compare the Average Sale Prices by Neighborhood

1. *groupby* the data by year and neighborhood and aggregate the results by the *mean* of the groups.
2. Drop **housing_units** column to show only the **sale_price_sqr_foot** and **gross_rent** throughout the period. 
2. Use *hvplot* and *groupby* function to plot the **Sale Price Per Square Foot and Average Gross Rent from 2010 to 2016 by Neighborhood**.

![<3>](<Image/bokeh_plot (2).png>)

*The average sale price per square foot for 2016 is less than the price in 2012 for Anza Vista neighborhood*.

---

## Build an Interactive Neighborhood Map

1. Read the **neighborhood_coordinates.csv** file and make a DataFrame named **neighborhood_locations_df**.
2. *groupby* the data by neighborhood and aggregate the results by the *mean* of the groups and create another DataFrame named **all_neighborhood_info_df**.
3. Use *concat* function to combine both DataFrames.
4. Use *dropna* and *rename* the column.
5. Use *hvplot* with *Geoview* to create point plot for **Sale Price Per Square Foot and Gross Rent from 2010 to 2016 by Neighborhood**.

![<4>](<Image/bokeh_plot (3).png>)

*Westwood park has highest gross rent of 3959, and Merced Heights has highest sale price per square foot of 788.845.*


---

## Conclusion

*The trends in both rental income growth and sales prices are increasing from 2010 to 2016 in a steady pace. However, the rental income is growing faster than the sale price in SF. It appears to have similar trend for all the neighborhoods across SF. However, the correlation is not always positive in all the area throughout entire time. For example, in Alamo Square, when the sale price drop from 2015 to 2016, the rent is still going up.*

*The potential one-click, buy-and-rent strategy helps clients to visualize and get a better understanding on the area with potential investment. For example, the size of the circle symbolizes the sales price, and the color of the dot symbolizes the gross rent. The bigger the circle, the higher is the sales price, and darker the dot is higher the rent. I do recommend to look for a smaller and darker dot on the graph for a potential investment. This means the neighborhood is having a cheaper sales price but a higher potential rental income. I do suggest an investment at Silver Terrace.*

---

## Contributors

Feier Ou 

ffeierou1003@gmail.com 

---

## License

Feier Ou 
