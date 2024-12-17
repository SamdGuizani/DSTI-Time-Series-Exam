The file 2023-11-Elec-train.xlsx contains electricity consumption (kW) and outdoor air temperature for a building. These quantities are measured every 15 minutes, from 1/1/2010 1:15 to 2/20/2010 23:45. In addition, outdoor air temperature is available for 2/21/2010. The goal is to forecast electricity consumption (kW) for 2/21/2010.

Two forecasts should be returned, in one Excel file entitled YourName.xlsx, with exactly two columns (one columns per forecast) and 96 rows:

1. the first one without using outdoor temperature,
2. the second one using outdoor temperature.

Of course, the goal is to get the best possible forecast. So you have to test all the models we saw during the course, to tune them and compare them correctly. In addition to your forecast, you should also return a short reports (few pages), entitled YourName.pdf, explaining how you have proceeded and containing the R codes you used.

The grading will take into account:

* the quality of your methodology (50%)
* the quality of your forecast (30%)
* the quality of your report and the respect of the exam instructions (20%)

A bonus grading of 15% can be obtained if you manage to obtained coherent results using a Deep Neural Network in R (coherent means comparable to what you obtained with other models). To obtain this bonus, a separate YourName.Rmd file should be submitted.
