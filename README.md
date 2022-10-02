# Homework #2 "It's getting hot in here..."

![Globe](https://github.com/tkelley3/hw2/blob/master/climatechange.jpg)

## Outcomes
- Import large data files 
- Export processed data to multiple file formats
- Create graphs illustrating trends in data

## Problem 
Importing and processing data is an important skill to master, especially if you find yourself in the industry dubbed "Big Data". Today, you will be processing data from `GlobalTempbyYear.txt` (format of which is location at https://www.metoffice.gov.uk/hadobs/hadcrut4/data/current/series_format.html) and `GlobalCarbonBudget2020.xlsx` (which has extensive documentation in the file). These files contain global temperature averages and carbon emission data respectively. Both are rich datasets that we may return to, but right now we want a small slice of data from each file. **Writing a script in `MATLAB` called `climate.m` doing the following**:
 
1. Import the data from the *Historic Budget* sheet in the `GlobalCarbonBudget2020.xlsx` and the columns (year, temperature anomaly smooth, and the last two columns in the file) from `GlobalTempbyYear.txt`. (Note the first year in `GlobalTempbyYear.txt` is 1880. )
1. Calculate the **cumulative sum** of the columns labeled `fossil emissions excluding carbonation` and `land-use change emissions` in `GlobalCarbonBudget2020.xlsx` through the years starting with the year 1850. This cumulative sum of carbon emissions should still have values for each year. For instance, the value for 1860 should be the sum of all carbon emissions from 1850 to 1860 (you may want to look at the function `cumsum` in MATLAB.)
1. Create a `table` containing the columns year, `fossil emissions excluding carbonation` emissions, `land-use change emissions`, the cumulative sum of carbon emissions, the average global temperature, and the lower and upper bounds of the 95% confidence interval of the combined effects (these are the last 2 columns of `GlobalTempbyYear.txt`).
1.Produce 3 graphs: (i) a `plot` of the global temperature and the cumulative sum of carbon emissions vs the year on the same plot using two y axes, (ii) and a `plot` of the global temperature, with error bars indicating the 95% confidence interval, and the cumulative sum of carbon emissions vs the year on the same plot using two y axes (iii) a `scatterplot` of the temperature vs the cumulative sum of carbon emissions.    
1. Save this data to a data file called `climate.mat`.
1. Write this table to a file called `climate.txt`.
