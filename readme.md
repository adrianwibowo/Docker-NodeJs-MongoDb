- `npm -v` make sure npm installed
- `npx express-generator` to get express boiler plate
- `npm install` to install the dependencies
- add `.gitignore` file and write `/node_modules` to exclude node_modules uploaded to repositories
- add docker workspace and file with VScode docker plugin( choose: Nodejs, and package.json )
- add `nodemon` packages and change start script at package.json
- Write services(Nodejs & Latest Mongodb Image) on `docker-compose.yml`and run `docker-compose-up`
- `docker start <name of this project mongodb container name>` later u just use `docker-compose up` to run your collection
- go in Mongo Shell `mongo` (not yet secured)
- create database with `use <yourdb namme>`
- insert initial data, in this case 
    ```
    db.Todos.insertMany([
      { 
        description: 'Go to laundry',
        complete: true
        }
      { 
        description: 'Go Fishing',
        complete: false
        }
    ])
    
    ```
- next we install mongoose in order to retrieve the data from database and display it to views `npm install --save mongoose
- Add mongoose configuration on `app.js` and create models folder and write new file `Todos.js` then define the models.
- adjust `index.js` at router import models and create `find()` function to retrieve `collection` and display it.
