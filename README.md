# Getting Started

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
