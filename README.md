# relative-humidity-in-r
This is a Time Series Analysis End Term Project provided by Indian Institute of Technology, Madras (IITM). 

## Question Description
The objective of your project is to predict relative humidity using FTS modelling and compare the forecasts with a standard optimally tuned SARIMA model that takes temperature as
exogenous regressors. The specific instructions for the project follow after a description of the
data below.
Data is obtained from an Automated Weather Station (AWS) located at Sriharikota during the
period May 15 - July 07, 2009. The data set comprises measurements of different meteorological
variables namely, air temperature, wind speed, wind direction, atmospheric pressure, relative
humidity (RH), rainfall and sunshine. In addition, other meta details such as the station code,
latitude / longitude, date and time of measurements are included.

1. Read the data into R using the read.csv routine (you may use the "Import Dataset" option
in RStudio). Ignore the first four columns for the remainder of analysis.
2. Observe that the data is missing at different date / time locations. Write an R script that
identifies these missing locations based on the TIME column and inserts “NA” for corresponding
values in the variables.
3. Use your favourite missing data replacement algorithm to impute (“fill in”) the missing observations. Partition the data into training and test data for model fit and validation, respectively. For
this purpose, you may reserve the last 96 observations (four days of data) for cross-validation.
4. Create TS objects for RH and temperature variables, respectively.
5. Build the best fuzzy time-series model by either writing your own R script or using the
AnalyzeTS package. Call the resulting model M1. Report all your findings, especially the
forecast metrics. Discuss the goodness of your model.
6. Develop a linear SARIMA model with temperature as the exogenous input to RH. Determine
the appropriate past values of temperature to be included using a mix of cross-correlation
analysis and trial-and-error approach. Call this model M2. The procedure (for developing the
model) should be systematic and include all checks. Report the model and all other relevant
details.
7. Compare the forecasts of M1 and M2 on the basis of training and test performance to select
the better model among the two. Provide suitable justification for your choice.
8. Using the model that you select in Step 7, replace the imputed values in Step 3 with their
predictions. Re-build the model with this interpolated data. Does the resulting model and / or
the forecasts appear any significantly different from its predecessor? If yes / no, why?
