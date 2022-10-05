# Natours-server
Natours(a tour-booking site) API for users, tours, reviews which does CRUD operations with advanced feauters like Authorization,

## Tech Stacks:
- Node.js,Express.js (Server Side).
- MongoDB{NoSQL} (DataBase).

## Getting started:
- Firstly, hit `npm install` to install all node_modules. 
- Then, hit `nodemon server.js` or `npm start` to start server.
- It will Firstly, chooses a port(which will be displayed on console) and runs on it.
- Secondly, it connects to the **Local MongoDB** by current IP address, and creates a new DB called *Natours*.
- for importing quick data, go to /dev-data/data , and run `node import-dev-data.js --import` by considering one model at a time in the file.
- If you decide to delete the data from DB, run `node import-dev-data.js --delete` considering each model at a time in the file.


## Brief Description: 
- **Models**: 
Basically,this app contains tour,user,review models in it.

- **Controllers**: 
The Controllers are designed such a way that server basically does CRUD operations on Models with Certain authorizations only, along with some special features such as delete the current user, get the current user,etc. Added even the Geometric coordiantes from **mongoose** Library, which is used to get minimum tours that are within specific radius through a route in tourRoutes.js.

- **MiddleWares**: 
Used middlewares such as basic app middlewares for security and parsing puprposes, and then jwt middlewares for getting user access to do such permissions, and then mongoose middlewares for MongoDb manpulations.

- **Authorization**:
With the help of **jwt**(Json Web Token), we can get authorized.Such as, tour CRUD operations(only through auth) in mongoDB,and even users CRUD(only if user is logged in),and in emergency situations such as reset password, forgot password via mailing through *mailtrap.com*.

### Note:
 **Postman's Documentation - by publishing [here](https://documenter.getpostman.com/view/21503860/2s83zdw66C). You can read all the API's detailed documentation** 