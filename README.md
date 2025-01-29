# DapperDotNetCoreApi

About Dapper
Dapper is an ORM (Object-Relational Mapper) or, more precisely, a Micro ORM, which we can use to communicate with the database in our projects. We can write SQL statements using Dapper as we would in the SQL Server. Dapper performs well because it doesn’t translate queries we write in .NET to SQL. It is important to know that Dapper is SQL Injection safe because we can use parameterized queries, which we should always do. One more important thing is that Dapper supports multiple database providers. It extends ADO.NET’s IDbConnection and provides useful extension methods to query our database. Of course, we have to write queries compatible with our database provider.


When discussing these extension methods, we must say that Dapper supports synchronous and asynchronous method executions. We’ll use the asynchronous version of those methods.

About Extension Methods
Dapper extends the IDbConnection interface with these multiple methods:

Execute – an extension method that we use to execute a command one or multiple times and return the number of affected rows
Query – with this extension method, we can execute a query and map the result
QueryFirst –  it executes a query and maps the first result
QueryFirstOrDefault – we use this method to execute a query and map the first result or a default value if the sequence contains no elements
QuerySingle – an extension method that executes a query and maps the result.  It throws an exception if there is not exactly one element in the sequence
QuerySingleOrDefault – executes a query and maps the result or a default value if the sequence is empty. It throws an exception if there is more than one element in the sequence
QueryMultiple – an extension method that executes multiple queries within the same command and maps results
As we said, Dapper provides an async version for all these methods (ExecuteAsync, QueryAsync, QueryFirstAsync, QueryFirstOrDefaultAsync, QuerySingleAsync, QuerySingleOrDefaultAsync, QueryMultipleAsync).

Database and Web API Creation and Dapper Installation
Before using Dapper in our project, we must prepare a database and create a new Web API project. So, let’s start with the database.

Once we have our table and the data, we can create a new Web API project.

With our project in place, we can install two required packages:

Dapper – PM> Install-Package Dapper

SQL Client – PM> Install-Package Microsoft.Data.SqlClient

We’ve learned how to integrate Dapper into the ASP.NET Core project and how to use queries, executions, stored procedures, and transactions with Dapper.