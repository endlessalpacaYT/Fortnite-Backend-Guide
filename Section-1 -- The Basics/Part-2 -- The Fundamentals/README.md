# Part-2 -- The Fundamentals

## Part Description:
- Part-2 -- The Fundamentals : In this part you will learn alot of core features of express.js since that is the web framework we will be using in this guide, this part will not have alot but it will have enough to get you going with knowledge on creating basic routes, getting data from the request and sending back a response!

## Express.js Fundamentals:
### Creating Routes!
Example Route:
```javascript
// example route for the contentpages route for fortnite
express.get('/content/api/pages/*', (req, res) => { // the "*" represents a wildcard
    // Your Logic Here...
})
// Or you can make an asyncronous route
express.get('/content/api/pages/*', async (req, res) => { 
    // Your Logic Here...
})
```
### Extracting The Data From The Request And Sending A Response:
Example:
```javascript
express.get('/content/api/pages/*', (req, res) => { 
    // Extracting the data from the request body:
    const { accountId, username } = req.body;
    // Extracting the data from the request params, e.g: the route is '/fortnite/:accountId/:username'
    const { accountId, username } = req.params;
    // Extracting the data from the request query, example request: http://127.0.0.1:3551/account?accountId=whatever&username=pongo
    const { accountId, username } = req.query;

    // Sending a response back:
    res.send({
        status: "OK",
        code: 200
    })
    // Or sending a response with a status code:
    res.status(200).send({
        status: "OK",
        code: 200
    })

    // NOTE: these responses or being sent in a json format.
})
```
### Setting And Getting Headers:
```javascript
express.get('/content/api/pages/*', (req, res) => {
    // Setting a custom header
    res.set('Custom-Header', 'HeaderValue');

    // Getting a header
    const authHeader = req.headers['authorization']; // Commonly used for authentication tokens

    // Setting multiple headers
    res.set({
        'Custom-Header': 'HeaderValue',
        'Another-Header': 'AnotherValue'
    });

    // Setting standard headers, like Content-Type or Authorization
    res.set('Content-Type', 'application/json');
    res.set('Authorization', 'Token69');

    // Sending a response back with headers set
    res.status(200).send({
        status: "OK",
        code: 200
    });

    // NOTE: dont worry about these too much you wont be using them that much!
});
```

### Starting Your Express Server:
```javascript
// Require your express package
const express = require("express");
const app = express();

// Define a route
app.get('/', (req, res) => {
    res.status(200).send({
        status: "OK",
        code: 200
    })
})

// Start the express server
app.listen(3551);
// Or do it like this with a log:
app.listen(3551, () => {
    console.log("Express Server Started");
})

// NOTE: 3551 can be changed to whatever port you would like e.g: app.listen(8080); will also work it will just start the express http server on port 8080 instead of 3551, To test your code go onto your browser and go to http://127.0.0.1:PORTNUMBER/ Replace PORTNUMBER with the port you chose
```

## Congrats you just completed this part, I hope this helps you and if you are enjoying the tutorial so far please considering giving this repo a star!