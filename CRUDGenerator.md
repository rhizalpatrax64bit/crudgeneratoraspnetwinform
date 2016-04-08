# Introduction #

This is a WINFORM CRUD SPROC and C# code Generator built using Visual Studio 2008.  It is a tool which will automatically create stored procedures in the SQLServer database and C# code to handle common CRUD data manipulation

This tool will automatically create stored procedures and C# code to handle common data manipulation operations:
  1. **C** r e a t e
  1. **R** e a d
  1. **U** p d a te
  1. **D** e l e t e

The purpose of this tool is to speed up development by leveraging the database schema as a starting point for C# objects.  It also creates a Data Layer which integrate nicely with the generated stored procedures and Business Layer.

The business layer is the C# object which the table columns as its properties.  Any additional behaviors can be added to this class.

The data layer implements the communication with the database, thereby insulating the data object from the internals of the specific database with which we are communicating.

And lastly the Crud Generator also builds a data access layer which handles the command execution against the database.

# History #
Initially I downloaded the code for the stored procedure generator portion from http://www.codeproject.com/KB/database/CRUD_Generator.aspx

My contribution:
  * The ability to provide usernames and passwords so as to connect to remote database.
  * A checkbox to run drop if exists clauses on stored procedures
  * Tweaked the query which returns the list of columns in tables so as to exclude timestamp columns and better handle nvarchar columns.
