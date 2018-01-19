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
        
  ##### Efficient INSERT queries through node
        
        var person = {
            email: faker.internet.email(),
            created_at: faker.date.past()
        };

        var end_result = connection.query('INSERT INTO users SET ?', person, function(err, result) {
            if (err) throw err;
            console.log(result);
        });
        
        mysqljs package automatically convert the query into correct MYSQL query and then excuted in mysql server.
        
   SIDENOTE: Even below code is perfectly correct.
            
            var q = 'INSERT INTO users (email) VALUES ("rusty_the_dog@gmail.com")';

            connection.query(q, function (error, results, fields) {
            if (error) throw error;
            console.log(results);
            });
