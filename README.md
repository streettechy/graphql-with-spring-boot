# Why GraphQL?
GraphQL is a query language for REST API endpoints.  GraphQL isn’t tied to any specific database or storage engine. Instead, GraphQL is backed by your existing code and data.

The main advantage of using GraphQL are:
````
No need to create multiple API (Application Programming Interface) endpoints in an application unlike in REST where we expose multiple endpoints to retrieve data like this.
https://localhost:8080/vehicle 
https://localhost:8080/vehicle/{id}
````

Using GraphQL, we get the exact data we need or request. This is unlike in REST implementation, where we make an HTTP GET call to get a JSON response even if we are looking at the values for a few attributes. For example, when we query a REST API, we get the complete response in JSON format like below even we require only the id and name
````
{"id": "1","modelCode": "ABC1234","brandName":XYZ","launchDate": "2020-05-30"}
````

# Testing the Application

Open this link — http://localhost:8080/graphiql 

# Run the following query to create a vehicle
````
mutation {
  createVehicle(type: "bus", modelCode: "ABC1234", brandName: "XYZ", launchDate: "2020-05-30") 
  {
    id
  }
}
````

# Run a query to get the data

````
query {
  vehicles(count: 1) 
  {
    id, 
    type, 
    modelCode
}
}
````
