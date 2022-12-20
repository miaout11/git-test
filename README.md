# Simple Twitter API  
A RESTful API server for Simple Twitter project built with Node.js, Express framework, and MySQL.  

**Simple Twitter API** is hosted on Heroku now. You can give it a try by using following base URL.  
```
https://quiet-mountain-47605.herokuapp.com/
```

**Simple Twitter Demo** is hosted [here](https://yuwen-ctw.github.io/simple_twitter/login). You can use the following accounts to login and try all the features:  
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
### Prerequisites
Node.js, Express and MySQL are installed.

### Installing
#### Clone the repo  
```
git clone https://github.com/miaout11/twitter-api-2020
```
#### Install dependencies  
```
npm install
```
#### Create file and folder in root  
* Create a `.env` file and set variables(see `.env.example`). Notice that `JWT_SECRET` is required and `IMGUR_CLIENT_ID` is optional.
* Make a `temp` folder for image upload feature.  
#### Setting for database  
* Modify `/config/config.json`
```
"development": {
  "username": "root",
  "password": "password",
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
