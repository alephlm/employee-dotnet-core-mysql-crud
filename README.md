# Dotnet core and mysql CRUD example

### This is an API CRUD example for an .net core 2 application using mySql database for storing data.

#### Configuration:
- This project is using a mysql db. You need to change the the connection string property `EmployeeDatabase` in `appsettings.json`, according to your local configuration.

#### Migration
- For the fist execution you need to run migrations for creating db tables.
- execute: `dotnet ef migrations add InitialCreate` than
- execute: `dotnet ef database update`.

#### Running
- To run the project execute `dotnet run`.
- It will be avaliable on `https://localhost:5001/api/`.

#### Executing actions
- To retrieve all employees: GET request to `https://localhost:5001/api/Employee`
- To retrieve specific employee: GET request to `https://localhost:5001/api/Employee/{employeeID}`.
- To create one employee: POST request to `https://localhost:5001/api/Employee`. with json data in body request
```
{
  "name": "Jon",
  "department": "Finance",
  "title": "Buyer"
  "isActive": true
}
```
- To update a employee: PUT request to `https://localhost:5001/api/Employee/{employeeID}`. with json body including the compleat object in body request.
```
{
  "id": 1, 
  "name": "Jon Snow",
  "department": "Finance",
  "title": "Manager"
  "isActive": true
}
```
- To delete one employee: DELETE request to `https://localhost:5001/api/Employee/{employeeID}`.