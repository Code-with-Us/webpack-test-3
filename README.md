# README

## Goal

In this third test, we're going to add two scripts to the scripts section of our package.json file. We can use these scripts in place of webpack and webpack-dev-server command line commands, which can sometimes take several options that would be tedious to re-type over and over again. 
    
We're also going to combine the work we did in test 1 and test 2, so that we can deploy our app either from the dist folder or (during development) from the dev server.

## Picking up from Exercise 2

As in exercises 1 and 2, we've initialized our project and installed webpack, webpack-cli, and webpack-dev-server. 

We have the same minimal html.index file and the same 'src' directory in which we've placed our index.js file and a second file called hello.js. index.js imports hello.js and calls it from within a console.log statement. hello.js returns a greeting, e.g. "Hello, Julian". 

## Adding NPM scripts

Now let's open package.json and insert the following:

```bash
    "scripts": {
        "build" : "webpack --mode production"
        "start:dev" : "webpack-dev-server --hot",
    },
```
    
We can now use the command 'npm run build' in place of 'npx webpack --mode production,' and 'npm run start:dev' in place of 'npx webpack-dev-server --hot.'

As in exercise 2, in index.html our script src points to 'main.js,' but we can change that './dist/main.js' when we want to deploy the production build of our app.

