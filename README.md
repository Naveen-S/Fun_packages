# Fun packages
All the packages I have come across!!

### Faker
https://github.com/marak/Faker.js/

  Faker is used to generate massive amount of fake data!
    
  ex: 
    Generating a random emailId and address
    
    var faker = require("faker");

    console.log(faker.internet.email());
    console.log(faker.address.streetAddress());
    console.log(faker.address.city());
    console.log(faker.address.state());
    

output: 
       
        Antonina_Eichmann@yahoo.com
        850 Oberbrunner Burgs
        South Schuylerton
        Florida



### MYSQL
  https://github.com/mysqljs/mysql
  
  To include in your package:
        
          npm install mysql
   
   Initial setup and test query:
        
        var mysql = require('mysql');

        var connection = mysql.createConnection({
        host     : 'localhost',
        user     : 'naveen',  //your username
        database : 'join_us'         //the name of your db
        //password : "if necessary"
        });
        
        connection.query('SELECT 1 + 1 AS solution', function (error, results, fields) {
        if (error) throw error;
        console.log('The solution is: ', results[0].solution);
        });
        
