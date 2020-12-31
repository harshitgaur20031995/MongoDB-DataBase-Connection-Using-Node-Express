# MongoDB-DataBase-Connection-Using-Node-Express
# MongoDb DataBase Connection Node.js Express.js
# install Express Using Command `npm i express`


`const express = require('express');
const mongoose = require("mongoose");
const app = express();

//dbconnection is my DataBase Name  
//first create your databse

const port = process.env.PORT || 3030;
mongoose.connect('mongodb://localhost:27017/dbconnection', (err) => {
    if (!err)
        console.log('MongoDB connection succeeded.');
    else
        console.log('Error in DB connection : ' + JSON.stringify(err, undefined, 2));
});


app.listen(port,()=>{
    console.log('server is connected as : '+port);
})`
