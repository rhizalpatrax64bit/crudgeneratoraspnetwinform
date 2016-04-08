# Introduction #

As I make some changes and assumptions, I will add them here.


## SPROC CRUD GENERATOR (Development version) ##
I will be putting unreleased changes here.  Nothing for today.

## SPROC CRUD GENERATOR v1.0.6 ##
### Oct. 15, 2009 ###
  * Added a data access layer to take care of all communication with the database
  * Enhanced the dataReader extension methods by adding a ToChar and ToBool function which takes one parameter to be converted to boolean.
  * Bug Fix: Loading a saved session now makes sets the option check boxes toggle accordingly.
  * The version number now shows up in the main window.

## SPROC CRUD GENERATOR v1.0.5 ##
  * Added support for varchar(max)
  * fixed column size issues with nvarchar.  This was tested against SQLServer 2008, where the column size was reporting as length 200 for nvarchar(100).
  * added the Go statement to each TSQL statement when output to file is selected.
  * Added awareness of calculated columns when generating sprocs and when passing parameters from the datalayer.
  * Added very basic ability to save the current working session information so you don't have to enter the username, password, table name filter, and output directory each time you run the application.

## SPROC CRUD GENERATOR v1.0.4 ##
  * The generate drop if exists checkbox is now off by default - since it might overwrite customized content.
### TODO ###

  * Wire up a stored procedure prefix textbox
  * wire up the Data Access Layer
  * Wire up the data layer to use stored procedures for input and the data access layer to talk to the database.
  * WIre up the Business object to use the data layer.


## C# CRUD GENERATOR ##