Here, a REST API is being created from scratch using simple vanilla node.js to demonstrate the fundamental principles of a REST API.

1. we need a json file with products to imitate a database where we can request data from >> data/products.json
2. then initialize a package.json >> npm init -y
3. to monitor the server.js we need a monitoring tool >> npm i -D nodemon
4. create these starting scripts:
   "start": "node server.js",
   "dev": "nodemon server.js"
5. create server.js as an entry-point with:
   - http - module (comes with node.js) and then as method to start the http-server >> const http = require('http')
   - products - import to GET the data from the server >> const products = require('./data/products')
6. with postman check the GET response >> all products shown up
7. to create the different routes we use models and controlers
