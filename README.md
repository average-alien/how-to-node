# How to Node

## Building your own module

1. First, create a .js file which will contain the code for our module
2. Write the code we want to export using the object `module.exports`

```
    // examples
    module.exports.myFunction = () => console.log("Fetch is not happening")

    module.exports.someNumbers = [39, 2, 56]
```

3. Import the module into another .js file using the `require()` function which takes the file path of the module we want as an argument

```
    // example
    const myModule = require('./myModule.js)

    myModule.myFunction()
```
4. We can use any code contained in the module by using dot notation

## Cloning a repo that uses node packages

1. Clone down the repo that you want to work with
2. There should be a file called `pacakge.json` that contains a list of "dependencies" which are node packages the repo used
3. By going into our terminal and using the command `npm install` in the directory of the repo, we can download all the neccessary packages to our local repo
4. npm is able to look at the `package.json` file and read the list of dependencies to install exactlly what the repo used and needs