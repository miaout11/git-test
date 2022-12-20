# Simple Twitter API  
A RESTful API server for Simple Twitter project built with Node.js, Express framework, and MySQL.  
The apis are hosted on Heroku now.
You can give it a try by using following base URL.  
```
https://quiet-mountain-47605.herokuapp.com/
```
**Demo** is hosted [here](https://yuwen-ctw.github.io/simple_twitter/login). 
You can use the following accounts to login.  
```
User(前台)
account: user1
password: 12345678

Admin(後台)
account: root
password: 12345678
```
## API Documents  
* [API Documents](https://gabby-chimpanzee-de2.notion.site/API-Documents-8fbcef78100c4d3ebde095c3031a0856)  

## Satrt to build a local API server  
### Please make sure you have installed Node.js, Express and MySQL.
#### Clone the repo  
```
git clone https://github.com/miaout11/twitter-api-2020
```
#### Switch to folder  
```
cd twitter-api-2020
```
#### Install 
```
npm install
```
#### Create file and folder in root
##### Set .env
* Create a `.env` file and set variables(see `.env.example` file).
``` 
JWT_SECRET=
IMGUR_CLIENT_ID=
```
##### Set upload feature
* Create a `temp` folder for image upload.
#### Setting for database  
* Modify `/config/config.json`
```
"development": {
  "username": "root",<change to your mysql username>
  "password": "password",<change to your mysql password>
  "database": "ac_twitter_workspace",
  "host": "127.0.0.1",
  "dialect": "mysql"
}
```
* Create database to your MySQL  
```SQL
CREATE DATABASE ac_twitter_workspace;
```
* Migrations and seeds(run in terminal)  
```
npx sequelize db:migrate
npx sequelize db:seed:all
```
### Start the server  
```
npm start
```

## Built With  

* [Express](https://expressjs.com/) - The framework used  
* [MySQL](https://www.mysql.com/) - Database  
* [Heroku](https://www.heroku.com/platform) - Where API hosted  

## Authors  
* [Evelyn](https://github.com/miaout11)  
* [Timothy](https://github.com/Coli-co)  
