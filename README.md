# Branch 'branch-add-faker'

Steps:
    
  goto node-project (base template), if not installed, clone it!
  
  cd node-project

  * You must install 'faker' package *
  npm install faker --save

  Open file app.js
    
    Add this:
    
      const faker = require('faker')
      ...
      ...

      // ADD THIS TEST ENDPOINT
      app.get('/vehicles', function (req, res) {
         let arr = [];
         let antenas = [];
         for (let i = 0; i < 50; i++) {   
            arr.push(            
               {   
                  vehicle: faker.vehicle.vehicle(),
                  manufacturer: faker.vehicle.manufacturer(),
                  model: faker.vehicle.model(),
                  type: faker.vehicle.type(),
                  fuel: faker.vehicle.fuel(),
                  vin: faker.vehicle.vin(),
                  color: faker.vehicle.color()
               }            
            );
         }

         let result = {
            vehicles: arr
         }
         res.setHeader('Content-Type', 'application/json');
         res.end(JSON.stringify(result));
      });

  Save changes

  Execute node app.js

  From browser

    Navigate to http://localhost:3000/vehicles

That's all !!

Link to faker: https://www.npmjs.com/package/faker
