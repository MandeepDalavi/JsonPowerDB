# Demo Project for JsonPowerDB!

> #### This project performs all the basic *CRUD* operation on JsonPowerDB

## About JsonPowerDB
JsonPowerDB is a Real-time, High Performance, Lightweight and Simple to Use, Rest API based Multi-mode DBMS. JsonPowerDB has ready to use API for Json document DB, RDBMS, Key-value DB, GeoSpatial DB and Time Series DB functionality. JPDB supports and advocates for true serverless and pluggable API development.

### Some Features of JsonPowerDB
- Nimble, Simple to use, In Memory, Real-Time
- **Schema free** - easy to maintain
- **Serverless Support** - fast development - cuts time to market
- **Multi-Mode** database - one solution to variety of data
- Build around worlds fastest* indexing engine **PowerIndex**
- Webservices API - low development cost
- A single instance - **Million Indexes**
- Inbuilt support to Querying Multiple Databases
- Multiple security layers
- **Server Side** Native **NoSQL** - best performance

### Competitive Landscape
|Feature| MongoDB | MySQL | Redis | HBase | Influx DB | JasonPowerDB |
|--|--|--|--|--|--|--|
| Document DB | ✔️ | ❌ | ❌ | ❌ | ❌ | ✔️ |
| Key-Value DB | ❌ | ❌ | ✔️ | ❌ | ❌ | ✔️ |
| RDBMS | ❌ | ✔️ | ❌ | ❌ | ❌ | ✔️* |
| GeoSpatial | ❌ | ❌ | ✔️ | ❌ | ❌ | ✔️ |
| Time Series DB | ❌ | ❌ | ❌ | ❌ | ✔️ | ✔️ |
| Wide Column Stores | ❌ | ❌ | ❌ | ✔️ | ❌ | ✔️* |

### Use Cases
- Any software application that needs backend database
	- Dynamic web applications/Mobile/Desktop Apps
- All RDBMS Use-cases
- All Document DB Use-cases
- All Key-Value DB Use-cases
- Use-cases that needs GeoSpatial/Time-series Analytics
- Best suited to real-time application for data analytics
- Improve existing application reporting / analytics performance
- Live working HTMl templates

### Why Prefer JsonPowerDB ?
- Minimum Development Cost
- Minimum Time to Market
- Minimize the complexity of interoperability of different applications
- Maximum data processing performance
- Technology Futuristic
	- Fills gap from database to big-data
	- Pluggable with new algorithms
	- Pluggable and user defined API
- Minimize Total Cost of Ownership

## Basic commands

### Insert Single Record
- Some important points to keep in mind
	- Http Method : POST
	- Base URL : http://api.login2explore.com:5577
	- End-point URL : /api/iml 
- Syntax
	```
	{
		"token": <"connection-token">,
		"cmd": "PUT",
		<<"dbName": <"database-name">,>>
		<<"rel": <"relation-name">,>>
		<<"colsAutoIndex": <boolean-value>,>>
		<<"templateStr": <jsonTemplateStr>,>>
		"jsonStr": <jsonDataStr>
	}
	```
- Code Sample
	```
	{
		"token": "608862679|6881615562961411263|608862579",
		"cmd": "PUT",
		"dbName": "StudentDB",
		"rel": "student",
		"jsonStr": {
			"name": "user",
			"email": "user@gmail.com"
		}
	}
	```
- Demo
![Demo of Insert Command](/images/screenshots/insert.gif)


### Retrieve Single Record
- Some important points to keep in mind
	- Http Method : POST
	- Base URL : http://api.login2explore.com:5577
	- End-point URL : /api/irl 
- Syntax
	```
	{
		"token": <"connection-token">,
		"cmd": "GET",
		"dbName": <"database-name">,
		"rel": <"relation-name">,
		"jsonStr": {
			<"ColumnName":"JsonValue">
    	}
	}
	```
- Code Sample
	```
	{
		"token": "608862679|6881615562961411263|608862579",
		"cmd": "GET",
		"dbName": "StudentDB",
		"rel": "student",
		"jsonStr": {
			"name": "user"
		}
	}
	```
- Demo
![Demo of Insert Command](/images/screenshots/retrieve.gif)


### Update Single Record
- Some important points to keep in mind
	- Http Method : POST
	- Base URL : http://api.login2explore.com:5577
	- End-point URL : /api/iml 
- Syntax
	```
	{
		"token": <"connection-token">,
		"cmd": "UPDATE",
		"dbName": <"database-name">,
		"rel": <"relation-name">,
		"jsonStr": {
			<"recordNo">: {
				<"ColumnName": "NewJsonValue">|<"New-ColumnName": "New-Column-Value">
			}
		}
	}
	```
- Code Sample
	```
	{
		"token": "90937075|-31948812362179105|90938333",
		"cmd": "UPDATE",
		"dbName": "StudentDB",
		"rel": "student",
		"jsonStr": {
			"2":{
				"name": "Test Student",
				"email":"teststudent@gmail.com",
				"mobile": 7098162348
			}
		}
	}
	```
- Demo
![Demo of Insert Command](/images/screenshots/update.gif)


### Remove Single Record
- Some important points to keep in mind
	- Http Method : POST
	- Base URL : http://api.login2explore.com:5577
	- End-point URL : /api/iml 
- Syntax
	```
	{
		"token": <"connection-token">,
		"cmd": "REMOVE",
		"dbName": <"database-name">,
		"rel": <"relation-name">,
		"record": <record_number | [recNo1, recNo2....]>
	}
	```
- Code Sample
	```
	{
		"token": "401400726|-363956312424328770|401400726",
		"cmd": "REMOVE",
		"dbName": "StudentDB",
		"rel": "student",
		"record": 1
	}
	```
- Demo
![Demo of Insert Command](/images/screenshots/remove.gif)


## Project Status: Under Development
- I'll be adding some more operations to it
- In addition, if anyone wants to contribute in this repo, then create a **PR (Pull Request)**. I will be happy to add more into it. Thanks.!

## If you want to know more please visit following links
JsonPowerDB Intro Notes: <https://github.com/MandeepDalavi/JasonPowerDB>
JsonPowerDB Website: <https://login2explore.com/jpdb/index.html>