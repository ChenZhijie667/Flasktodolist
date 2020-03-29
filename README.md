# Flasktodolist


# How to run and use  
## Run
Open a terminal in the file directory  
activate virtual env:
```
venv\scripts\activate
```
Spin up a local server and serve this web service:
```
cd flasktodo
set FLASK_APP=main.py
flask run
```
## Use
***Transfer data in json format***  
Examples under curl:  
### add item
```
curl -X POST http://127.0.0.1:5000/item/new -d "{\"item\":\"Add a item\"}" -H "Content-Type:application/json"  
```
### get all items
```
curl -X GET http://127.0.0.1:5000/items/all
```
### get one item
**If there are spaces in the value you need to replace them with either + or with %20**
```
curl -X GET http://127.0.0.1:5000/item/status?name=Add+a+item
```
### update status
**Status can be Completed,Not Started,In Progress**
```
curl -X PUT http://127.0.0.1:5000/item/update -d "{\"item\":\"Add a item\",\"status\":\"Completed\"}" -H "Content-Type:application/json"
```
### delete item
```
curl -X DELETE http://127.0.0.1:5000/item/remove -d "{\"item\":\"Add a item\"}" -H "Content-Type:application/json"
```
