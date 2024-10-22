# Part-3 -- Getting Started

## Part Description:
- Part-3 -- Getting Started : This is the first part where you will be starting to develop your backend from scratch!

## Getting Started:
### Setting Up Your Express Server:
The first thing that you should do is create a http server

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
```
This code is from part 2. From now on you will not recieve that much code, instead this guide will explain to you how to acheive the goal.