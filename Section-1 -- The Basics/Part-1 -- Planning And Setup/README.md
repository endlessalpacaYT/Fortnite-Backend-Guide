# Part-1 -- Planning And Setup

## Part Description:
- Part-1 -- Planning And Setup : In this part we will be going over the planning of your custom fortnite backend and the setup, this will include: how you will lay your backend structure out, what programming language you will add in your backend and what features you would like to include!

## Planning:
- In your fortnite backend you will need to plan a few things first, you can always skip this step and go straight to setup but if you are new to Fortnite backends or any kind of backend overall it might be a good idea to go through this with yourself so you have a clear idea of how you will make your backend!

### The Backend Structure AKA: Project Structure:
This is what your backend structure may look like:
- **src/**: Where you will store your main files
    - **routes/**: Where you will store your route files
    - **utils/**: Where you will store functions and other useful utilities made by you
    - **config/**: Where you will store your config files
    - **responses/**: Where you may store some json files for cleaner code
- **.env**: Where you will store sensitive information or configuration information
- **index.js**: The main exectution point in your code

The way you lay out your backend structure is completely up to you, you do not have to follow the example above however it is a good starter for it.

### Tips For A Good Structure:
- Always keep things organised in files and folders
- Organise your functions in files to clean up your main file or to be reused from other files
- Seperate your main backend files in a "src" folder
### Things not to do:
- Do not have everything in your main index.js file, while this is possible to have the whole backend in one file, It is not recomended for clean code, it will make your life alot easier to have everything organised in some way

### What Programming Language You Choose:
- Javascript (Node.js) : Good for beginner friendly coding experience, fairly easy to learn
- Typescript : Javascript with type safety, A little bit harder than javascript but is very similar
- Java Or C# : Generally alot harder to code in and learn, This programming is an object oriented programming language
- C++ : The hardest programming language to code in and learn, this programming language both supports functional programming and object oriented programming

### The Web Framework:
- Express.js : Really easy to learn, good for beginners
- Fastify : Also really easy to learn but a little bit harder, this framework tends to be faster

### This Guide Uses Javascript And Express.js But You Can Adapt This Guide Into Your Own Choice!

## Setup:
- This guide will teach you how to set up your environment ready to program in!

The setup is not hard, Simply open up a command prompt in your project folder and run the command ```npm install fastify.js``` Yes thats right, its that simple, Look at the features section in this readme below if you want more features in your backend!

### Features:
If you would like to have certain features in your backend there are packages for them!

- Database Integration : For beginner friendly database integration use mongodb, to include mongodb in your backend make sure to also run the command ```npm install mongoose```!
- A .env file : generally recomended to have in your backend so to include this package in your backend run the command ```npm install dotenv```!

### Including these packages in your code:
To use your packages that you installed using the command line make sure you follow the steps below

### Put this code in your index.js or whatever your main file is below:
```javascript
const express = require("express");
const app = express();
```
To add whatever feature you added before add this code:
```javascript
const mongoose = require("mongoose"); // const yourpackagename = require("yourpackagename");
// for using your env in your file you do it a little differently
require("dotenv").config(); // make sure you have a .env file!
```

## Congrats you just completed this part, I hope this helps you!