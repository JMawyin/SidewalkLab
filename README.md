# SidewalkLab

## Sidewalk Lab Tech Challenge

The are two files of interest in this depository:

Archive.zip   : Contains the *.csv* files used in the analysis download from the UN Energy Database

SidewalkLab_v3.ipynb  : Is the Python notebook with a link to Google Colab on top.

The Python notebook answers two question posed by the Sidewalk Lab team:

### Q1: For 2018, what was the percentage of the World’s electricity generation by the following sources - Coal, Oil, Natural Gas, Biofuels, Hydro, Nuclear, solar, and wind?

The solution was derived by first calculating the aggregating the generation per source globally (Q1.C, Q1.D and Q1.E) for the year 2018 and dividing by the aggregated global electricity generation for the same year (Q1.A) .

This first solution was wrong because the added generation percentages per source (Coal, Oil, Natural Gas, Biofuels, Hydro, Nuclear, solar, and wind) added to 160%. This is may be due to either the per country annual total generation being undervalued or the per source generation being overvalued. 

A new solution was arrived by adding up the global generation per source and using this a new *Total Generation* value. The new ratios using this value make more sense (Q1.F).


### Q2: For the decade spanning 2008-2018, what was the worldwide energy consumption by the following sectors - households, industry, transport, agriculture, and commercial / public services?

This solution was derived form the *Total Electricity* data set. First the rows in the table were filtered:

* First, to only include those in the range of (2008 to 2018 including). 
* Second, to only include rows with the string *Consumption*.
* Finally, again filtered to only include rows with strings in the list ['households', 'industry', 'transport', 'agriculture',  'commercial']

The rows were grouped by Transaction, Year and adding up the Quantity of Transaction.

The results were visualized using scatter plot, a wide format table and a heatmap to show the changes over time in generation per sector.

### Further Questions.

Insights on other questions of interest such as:

* What are the capacity factors per type of generator? Are the capacity factors comparable per country? Has there be an improvement during the last decade?
* In which country has the generation from renewables (wind, solar, hydro and tidal generators) surpassed generation from thermal generators (Coal, Oil, Natural Gas and Biofuels)?

Were provided in the notebook.
