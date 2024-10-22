# Part-4 -- Defining Routes

## Part Description:
- Part-4 -- Defining Routes : Time to start making some routes, we will focus on mocking them in section 1, in section 2 we will start to add some logic!

## What We Will Do:
### Learn how to make Routes in other files and connect them to your main file!
There are 2 things we must do to acheive this:
To Define a route file we must do this:
```javascript
app.use(require("./routes/whatever_route.js")); // Must provide the path to your route filegg
```
But wait we are not done, We must do this in our route file:
```javascript
// Require Express
const express = require("express");
const app = express();

// Define a route
app.get('/content/api/pages/*', (req, res) => { 
    // Your Logic Here...
})

// MUST ADD THIS PART!
// Export your routes
module.exports = app;
```
We will use this since we will organise our routes into a routes folder!

### Recomended actions:
add middleware for x-www-form-urlcoded and json:
Add in your Code:
```javascript
app.use(express.json()); // middleware for parsing json
app.use(express.urlencoded({ extended: true })); // middleware for parsing x-www-form-urlcoded
```
Make sure to add these before your route definitions!

Add error handling middleware:
```javascript
app.use((err, req, res, next) => {
    console.error(`Error occurred: ${err.message}`);
    res.status(500).send({
        status: "error",
        message: "Something went wrong!",
    });
});

app.use((req, res, next) => {
    res.on('finish', () => {
        if (res.statusCode >= 400) {
            console.error(`Issue with request: ${req.method} ${req.url} - Status: ${res.statusCode}`);
        }
    });
    next();
});
```
Add this after your route definitions, this error handling middleware will help you find errors in your code and missing routes!

### Whats Next!
Explore the folders in Part 4 these will help you with your routes!