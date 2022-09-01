# How to Node

## Starting a new project from scratch

- mkdir and cd into project directory
- run `npm init` to create `package.json` (can also use `npm init -y` to answer yes to all prompts)
- install needed packages with `npm install <package name>`
- create a `.gitignore` file and add `node_modules` to it
- make sure that `node_modules` is not being tracked by git

## Cloning a repo that uses node packages

- Clone down the repo that you want to work with and cd into the new directory
- There should be a file called `pacakge.json` that contains a list of "dependencies" which are node packages the repo used
- By going into our terminal and using the command `npm install` in the directory of the repo, we can download all the neccessary packages to our local repo
- npm is able to look at the `package.json` file and read the list of dependencies to install exactlly what the repo used and needs

### Building your own module (slightly misunderstood prompt)

- First, create a .js file which will contain the code for our module
- Write the code we want to export using the object `module.exports`

```
    // examples
    module.exports.myFunction = () => console.log("Fetch is not happening")

    module.exports.someNumbers = [39, 2, 56]
```

- Import the module into another .js file using the `require()` function which takes the file path of the module we want as an argument

```
    // example
    const myModule = require('./myModule.js)

    myModule.myFunction()
```
- We can use any code contained in the module by using dot notation