# node-express-server

# Create a Node with Express Project 
# https://codehandbook.org/building-node-js-express-app-using-typescript/

Steps:

  mkdir node-project 

  cd node-project

  npm init

  npm install express --save

  Create a file called app.js and add:

    Open

    Add:
    
      const express = require('express')
      const app = express()
      const port = 3000

      app.get('/', (req, res) => res.send("Welcome to setting up Node.js project tutorial!'))

      app.listen(port, () => console.log(‘Application listening on port ${port}!’))

    Save changes

  Execute node app.js

  From browser

    http://localhost:3000

That's all !!
