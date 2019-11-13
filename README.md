# qsql

Q SQL: IBM I - SQL client

Its a brower based SQL client for IBM I.

**Download or clone this repo.**

> For windows

1. Simply click on 1RUN.BAT file.

> For Linux/Mac/ Windows

1. point shell/cmd/powershell (or whatever its called) in that dir and use the following command
2. java -jar qsql.jar

It will open the url in your default browser.

**I.E. (any version) is not supported. Chrome and firefox only**

<hr/>

**Default**

> -user name : Admin

> -Password : AdminPass

> Port: 7007 and 7071

<hr/>

**Main Features:**

1. Inline-edits with @s query.
2. Copy data between servers with @copy query.
3. Option to save the query to use across multiple servers.
4. @table and @sp queries to view the catalog details.
5. Formatted and clean view of large datatypes like JSON and XML.
6. @multi to run multiple quries in one go.
7. Screen SQL: to build the quick screens for reusable sqls.
8. DB DOC: To document database tables.

<hr/>

**Features not included:**

1. calls for overloaded SPs.

 <hr/>

**Examples**

> lets say there are 2 servers with names Server1 and Server2. And system is currently connected to Server1.

> straight sql
> select \* from customer
> -this will display the customer data on screen.

- **double click** on any row will display that single row in vertical format.
- double click on any column (from the vertical row) will display that single column in sperate area.
- This is useful for big data types like JSON and XML.

> Joins

- Table header will contain the table name for each column if data is coming from multiple tables.

> **@s : inline Edit**

> @s customer

> @s customer where custid < 10

- this will give inline edit options for the customer table data.
- @s select \* from customer is not allowed

> @connect: connect to a differnt server to run the sql

> @connect Server2>> select \* from customer

- this will run the given query on "Server2"

> @multi: run multiple queries in one go.

> @multi @s customer && select _ from product && select _ from abc join xyz on a= b

- result for each query will be displayed in a seprate tab.

> @copy: copy data from one table to other (or across servers)

> @copy @from customer @to Server2>> customer2

> @copy @from select \* customer where custid>10 @to Server2>> customer2

- this will copy the customer data from Server1 to Server2

> @d: download the result as excel file.

> @d select \* from customer

- this will give the option to download the customer table data as excel.

> @b: kind of go to bottom

> @b customer where name like '%S%'

- display the latest record (by rrn) on top

  <hr/>

** Screen SQL **

TO DO\*\*

  <hr/>
![Image of QSQL](https://github.com/onlysumitg/qsql/blob/master/images/1.png)

<hr/>

![Image of QSQL](https://github.com/onlysumitg/qsql/blob/master/images/6.png)

<hr/>

![Image of QSQL](https://github.com/onlysumitg/qsql/blob/master/images/2.png)

<hr/>

![Image of QSQL](https://github.com/onlysumitg/qsql/blob/master/images/3.png)

<hr/>

![Image of QSQL](https://github.com/onlysumitg/qsql/blob/master/images/4.png)

>

<hr/>

![Image of QSQL](https://github.com/onlysumitg/qsql/blob/master/images/5.png)

<hr/>

ALL SOFTWARE IS PROVIDED “AS IS” WITHOUT ANY WARRANTY OF ANY NATURE WHATSOEVER. THE PROVIDER OF THIS SOFTWARE HEREBY DISCLAIMS ALL WARRANTIES, REPRESENTATIONS, AND CONDITIONS, STATUTORY OR OTHERWISE, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO WARRANTY OF TITLE AND THE IMPLIED WARRANTY OF MERCHANTABILITY AND FITNESS FOR A PARTICULAR PURPOSE. THE PROVIDER SHALL NOT BE LIABLE FOR ANY DAMAGES ARISING FROM OR AS A RESULT OF YOUR USE
OF THIS SOFTWARE. USE IT AS YOUR OWN RISK.
