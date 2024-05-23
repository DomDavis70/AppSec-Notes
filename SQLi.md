SQL injection (SQLi) is a web security vulnerability that allows an attacker to interfere with the queries that an application makes to its database.

Detection: 
	- The single quote character ' and look for errors or other anomalies.
	- Some SQL-specific syntax that evaluates to the base (original) value of the entry point, and to a different value, and look for systematic differences in the application responses.
	- Boolean conditions such as OR 1=1 and OR 1=2, and look for differences in the application's responses.
	- Payloads designed to trigger time delays when executed within a SQL query, and look for differences in the time taken to respond.
	- OAST payloads designed to trigger an out-of-band network interaction when executed within a SQL query, and monitor any resulting interactions.

Where can it occur:
	- Most SQL injection vulnerabilities occur within the WHERE clause of a SELECT query
	- In UPDATE statements, within the updated values or the WHERE clause.
	- In INSERT statements, within the inserted values.
	- In SELECT statements, within the table or column name.
	- In SELECT statements, within the ORDER BY clause.

Some Common SQL Injection Examples:
	- Retrieving Hidden Data - where you can modify a SQL query to return additional results.
		○ Take a query `SELECT * FROM products WHERE category = 'Gifts' AND released = 1`
![image](https://github.com/DomDavis70/AppSec-Notes/assets/42983767/de47f18a-3404-4063-8aa6-460217c596bd)

