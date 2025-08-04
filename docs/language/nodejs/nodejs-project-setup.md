# Set Up Node.js Projects

## Basic - Set Up A Simple Node.js Project

Create the folder to hold the project
```
mkdir my-project
cd my-project
```

Initialize the project
```
npm init -y
```

List and set configuration of the project
```
npm config list

npm set init-author-name "<My Name>"
npm set init-author-email "me@example.com"
npm set init-author-url "https://example.com"
npm set init-license "MIT"
```

Create the file index.js
```
touch index.js
```

Add the line to the file index.js
```
console.log("Hello World!");
```

Run the program - Method 1
```
node index.js
```

Add the entry start to package.json
```
{
  ...
  "scripts": {
    "start": "node index.js",
    "test": "echo \"Error: no test specified\" && exit 1"
  },
  ...
}
```

Run the program - Method 2
```
npm start
```

Install nodemon
```
npm install nodemon --save-dev
```

Change package.json
```
{
  ...
  "scripts": {
    "start": "nodemon index.js",
    "test": "echo \"Error: no test specified\" && exit 1"
  },
  ...
}
```

## Set Up with ECMAScript Features - Node.js with Babel

Install Babel for ECMAScript features
```
npm install @babel/core @babel/node --save-dev
```

Add to start script in package.json
```
{
  ...
  "scripts": {
    "start": "nodemon --exec babel-node index.js",
    "test": "echo \"Error: no test specified\" && exit 1"
  },
  ...
}
```

Install presets for Babel
```
npm install @babel/preset-env --save-dev
```

Create .babelrc file in the project's root folder
```
touch .babelrc
```

Include the recently installed dependency for upcoming JavaScript Features
```
{
  "presets": [
    "@babel/preset-env"
  ]
}
```

## References

1. [JavaScript Setup](https://www.robinwieruch.de/javascript-project-setup-tutorial/)
1. [Node.js with Babel Setup](https://www.robinwieruch.de/minimal-node-js-babel-setup/)

***
*Updated on 1 August 2025*
