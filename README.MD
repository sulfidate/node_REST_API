# Node REST API

> Full CRUD REST API using Node.js with no framework

This is a full REST API from scratch using simple vanilla node.js to demonstrate the fundamental principles of a REST API:

```
# Routes
GET      http://195.201.88.30:81/api/products
POST     http://195.201.88.30:81/api/products
GET      http://195.201.88.30:81/api/products/:id
PUT      http://195.201.88.30:81/api/products/:id
DELETE   http://195.201.88.30:81/api/products/:id

```

## Usage

```
I I have deployed a live server running the REST API.
You can easily query the routes provided above using POSTMAN.
```

# HowTo built

1.  - create json file with products to imitate a database where we can request and send data
      > data/products.json
    - initialize a package.json
      > npm init -y
    - to monitor the server.js
      > npm i -D nodemon
    - to create Id's automaticaly we need a tool uuid
      > npm i uuid
    - create starting scripts
      > "start": "node server.js", "dev": "nodemon server.js"
    - create server.js as an entry-point with
      - http-module (comes with node.js) as method to start the http-server
        > const http = require('http')
      - import products to GET the data from the server
        > const products = require('./data/products')

2.  - to create different routes use models and controllers = mvc-method (model-view-controller|view like react won't be needed as it's an pure api to test)
      - to interact with the model (get,put,delete data etc.)
        > controllers/productController.js
      - to handle the data
        > models/productModel.js

3.  - connect server.js to the mvc:
      > const { getProducts, getProduct, createProduct } = require('./controllers/productController')
    - connect utils.js to productModel to write data to file
      > const fs = require('fs')

4.  - create the routes in the productController:
      - GET allProducts = getProducts()
      - GET a single Product = getProduct()
      - POST data to the json = createProduct()
      - PUT update data by id = updateProduct()
      - DELETE deletes data by id = deleteProduct()

5.  Check all routes and functions with postman
    - Pics of all request are in the POSTMAN Folder
