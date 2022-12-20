# Simple Twitter API  
A RESTful API server for Simple Twitter project built with Node.js, Express framework, and MySQL.  

This is a collaborate project to make a simple Twitter web app. And the server-side API majors in authentication and data CRUD features.  


**Simple Twitter API** is hosted on Heroku now. You can give it a try by using following base URL.  
```
https://quiet-mountain-47605.herokuapp.com/
```

**Simple Twitter Demo** is hosted [here](https://yuwen-ctw.github.io/simple_twitter/login). You can use the following accounts to login and try all the features:  
```
Admin
account: root
password: 12345678

Users(provide 5 seed users)
account: user1 (~user5)
password: 12345678
```

**Simple Twitter Frontend** is developed by React.js ([repo link](https://github.com/Yuwen-ctw/simple_twitter)).  

## API Features  
### Authentication  
Check if the user is authenticated and authorized. Some routes are available to use after login, some are admin/user role only. Please refer to the API documents.  
### Admin  
* Signin background(後台)
* Get the list of all users  
* Get the list of all tweets  
* Delete tweet  
### Users
* Signin foreground(前台)
* Signup an new account  
* Post, like, reply or read a tweet  
* Follow, unfollow other users  
* Edit own profile(include upload avatar and cover)  
* Get data of a certain user(personal info, tweets, likes, followings, followers, replies)  

## API Documents  
* [API Documents](https://gabby-chimpanzee-de2.notion.site/API-Documents-8fbcef78100c4d3ebde095c3031a0856)  

## Build a local API server  
These instructions will get you a copy of the project up and running on your local machine for development and testing purposes.  

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
"username": <your mysql username>,
"password": <your mysql password>,
```
* Create database to your MySQL  
```SQL
CREATE DATABASE ac_twitter_workspace;
CREATE DATABASE ac_twitter_workspace_test;
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

## Auto-testing
There are auto-test files for models and requests in this repo. Look for more details in  `/test` folder.

### Set NODE_ENV before test  
```
export NODE_ENV=test  // macOS
set NODE_ENV=test  // windowsOS
```
### Run the tests  
```
npm run test
```
### Set NODE_ENV after test  
```
export NODE_ENV=developemnt  // macOS
set NODE_ENV=development  // windowsOS

```
### Check current enviornmment  
```
echo $NODE_ENV  // macOS
echo %NODE_ENV%  // windowsOS
```

## Built With  

* [Express](https://expressjs.com/) - The framework used  
* [MySQL](https://www.mysql.com/) - Database  
* [Heroku](https://www.heroku.com/platform) - Where API hosted  

## Authors  
* [Evelyn](https://github.com/miaout11)  
* [Timothy](https://github.com/Coli-co)  
