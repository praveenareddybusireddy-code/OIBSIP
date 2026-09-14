\# Task 3: SQL Injection



\## Objective



To understand and demonstrate an SQL Injection vulnerability using Damn Vulnerable Web Application (DVWA) in a controlled local lab environment.



\## Tools Used



\- Kali Linux

\- Apache Web Server

\- MariaDB

\- PHP

\- DVWA

\- Web Browser



\## Lab Environment



The SQL Injection test was performed only on a locally installed DVWA application using localhost.



\## Procedure



1\. Installed Apache, MariaDB, PHP, and required PHP modules.

2\. Downloaded DVWA into the Apache web directory.

3\. Created the DVWA database and database user in MariaDB.

4\. Opened DVWA using localhost.

5\. Created and reset the DVWA database.

6\. Logged in to DVWA.

7\. Set the DVWA security level to Low.

8\. Opened the SQL Injection module.

9\. Tested a normal User ID input.

10\. Tested a SQL Injection payload.



\## Normal Input



Input:



1



The application returned the record for the user with ID 1.



\## SQL Injection Payload



1' OR 1=1#



\## Result



The application returned multiple user records instead of only one record.



The condition `1=1` is always true. The `#` symbol comments out the remaining part of the SQL query in the MySQL/MariaDB environment.



\## Impact



SQL Injection may allow an attacker to:



\- Retrieve unauthorized database information

\- Bypass application restrictions

\- Modify or delete database records

\- Compromise sensitive information



\## Prevention



\- Use prepared statements and parameterized queries

\- Validate and sanitize input

\- Avoid directly concatenating user input into SQL queries

\- Use least-privilege database accounts

\- Display generic error messages

\- Perform regular security testing



\## Conclusion



The SQL Injection vulnerability was successfully demonstrated using DVWA in a controlled local environment. The exercise showed how unsafe handling of user input can cause unintended database results.

