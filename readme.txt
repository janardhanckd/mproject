GitHub location: https://github.com/janardhanckd/mproject/tree/master
Project Git location: https://github.com/janardhanckd/mproject.git
Envinorment :
SpringBoot, Spring JDBC, H2 in memory data base
Assigned port number using application.properties file
server.port=9091 -- Assigned the port number
customer.basepoints=1 -- reading the basepoints from properties files insted hard coding in the code, in future if we need to update the points just need to update the proeprty
customer.baseamount=50 -- added the base amout, for every $50 spent user will recieve 1 point.

Access the H2-console using http://localhost:9091/h2-console/
 - Created in customerdetails table
Created Below REST API for insert customer purhcases, getcustomer details, getMonthlycustomer rewards, getQuarterlycustomer rewards

1. Insert records using below service
POST Operation
http://localhost:9091/rewards/calculateRewards
Request body
[
	{
	"customerId":"C001",
	"purhcaseAmout":"500.00",
	"purchaseDate":"2022-04-01"
},
	{
	"customerId":"C002",
	"purhcaseAmout":"500.00",
	"purchaseDate":"2022-02-01"
},
	{
	"customerId":"C003",
	"purhcaseAmout":"500.00",
	"purchaseDate":"2022-03-01"
},
	{
	"customerId":"C004",
	"purhcaseAmout":"500.00",
	"purchaseDate":"2022-01-01"
},
{
	"customerId":"C002",
	"purhcaseAmout":"1500.00",
	"purchaseDate":"2022-02-01"
},

{
	"customerId":"C003",
	"purhcaseAmout":"110.00",
	"purchaseDate":"2022-02-01"
}

]


2. GET Operation
http://localhost:9091/rewards/getCustomerDetails/C002
this will give you the C002 customer details

3. GET Operation
http://localhost:9091/rewards/getQuarterlyRecords
this will give you the Quarterly records

4. GET Operation
http://localhost:9091/rewards/getMonthlyRecords
this will give you the Quarterly records


Used AOP concept to handle centeral exception handling.


