# Bulldozer-price-prediction-ML


## About Fast Iron
Fast Iron is creating a "blue book for bull dozers," for customers to value what their heavy equipment fleet is worth at auction.
Fast Iron are a content-focused business that aids customers in creating enterprise data standards, cleansing data, and maintaining clean data. Utilizing proprietary applications and an ever growing data cleansing team, Fast Iron has normalized data for more than 2.5 million machine and customer records for the heavy equipment industry.

This competition was launched under the Kaggle Startup Program: https://www.kaggle.com/competitions/bluebook-for-bulldozers

This project is for predicting the sale price of bulldozers sold at auctions.

The data for this competition is split into three parts:

* Train.csv is the training set, which contains data through the end of 2011.
* Valid.csv is the validation set, which contains data from January 1, 2012 - April 30, 2012 You make predictions on this set throughout the majority of the competition. Your score on this set is used to create the public leaderboard.
* Test.csv is the test set, which won't be released until the last week of the competition. It contains data from May 1, 2012 - November 2012. Your score on the test set determines your final rank for the competition.
  
The key fields are in train.csv are:

* SalesID: the uniue identifier of the sale
* MachineID: the unique identifier of a machine.  A machine can be sold multiple times
* saleprice: what the machine sold for at auction (only provided in train.csv)
* saledate: the date of the sale
* There are several fields towards the end of the file on the different options a machine can have.  The descriptions all start with "machine configuration" in the data dictionary.  Some product types do not have a particular option, so all the records for that option variable will be null for that product type.  Also, some sources do not provide good option and/or hours data.
The machine_appendix.csv file contains the correct year manufactured for a given machine along with the make, model, and product class details. There is one machine id for every machine in all the competition datasets (training, evaluation, etc.).


## Evaluation

The evaluation metric for this competition is the RMSLE (root mean squared log error) between the actual and predicted auction prices.

Sample submission files can be downloaded from the data page. Submission files should be formatted as follows:

* Have a header: "SalesID,SalePrice".
* Contain two columns.
* SalesID: SalesID for the validation set in sorted order.
* SalePrice: Your predicted price of the sale.
