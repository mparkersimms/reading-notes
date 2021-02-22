# Class 06 

references:

https://www.sitepoint.com/an-introduction-to-node-js/

By James Hibbard
JavaScript

February 16, 2020

## What Is Node.js?

stack overflow describes node.js as such:

- "Node.js is an event-based, non-blocking, asynchronous I/O runtime that uses Google’s V8 JavaScript engine and libuv library."

### Node Is Built on Google Chrome’s V8 JavaScript Engine

The V8 engine is the open-source JavaScript engine that runs in Google Chrome and other Chromium-based web browsers. It is responsible for compiling JavaScript directly to native machine code that your computer can execute.

- the creator of Node (Ryan Dahl) took the V8 engine and enhanced it with various features, such as a file system API, an HTTP library, and a number of operating system–related utility methods.

- Node.js is a program we can use to execute JavaScript on our computers.

### How Do I Install Node.js?

You can check that Node is installed on your system by opening a terminal and typing node -v. If all has gone well, you should see something like v12.14.1 displayed. This is the current LTS version at the time of writing.
- Then create a new file hello.js and copy in the following code:
    - `console.log("Hello, World!");`

    - `node hello.js` - should run and if node.js is installed properly is will display "Hello,World!"

### npm, the JavaScript Package Manager

To check which version you have installed on your system, type npm -v.
- npm is the world’s largest software registry

`npm install -g jshint` - will install the jshint package globally on your system

- Installing a Package Locally
    - `npm init -y` - This will create and auto-populate a package.json file in the same folder

    - `npm install lodash --save` - install the lodash package and save it as a project dependency

    - Create a file named test.js and add the following:
        - ```const _ = require('lodash');
            const arr = [0, 1, false, 2, '', 3];
            console.log(_.compact(arr));```

        - run the script using node test.js. You should see [ 1, 2, 3 ] output to the terminal

- Working with the package.json File
    - If you look at the contents of the test directory, you’ll notice a folder entitled `node_modules`. This is where npm has saved lodash and any libraries that lodash depends on. The node_modules folder shouldn’t be checked in to version control, and can, in fact, be re-created at any time by running npm install from within the project’s root.

    - By specifying your project’s dependencies in this way, you allow any developer anywhere to clone your project and use npm to install whatever packages it needs to run.

## What Is Node.js Used For?

installing (via npm) and running (via Node) various build tools — designed to automate the process of developing a modern JavaScript application

- Node.js Lets Us Run JavaScript on the Server

    - The Node.js Execution Model
        - when you connect to a traditional server it will spawn a new thread to handle the request.
        - The most common way to support more connections is to add more servers.
        - Node.js is single-threaded and event-driven
            - everything that happens in Node is in reaction to an event.

#### What Kind of Apps Is Node.js Suited To?

Node is particularly suited to building applications that require some form of real-time interaction or collaboration

#### What Are the Advantages of Node.js? 

You can do everything in the same language, which, as a developer, makes you more productive
- you can easily share code between the server and the client
- it speaks JSON
    - the most important data exchange format on the Web,

#### Other Uses of Node

it can be used as a scripting language to automate repetitive or error prone tasks on your PC

It can also be used to write your own command line tool, such as this Yeoman-Style generator to scaffold out new projects

- can be used to build cross-platform desktop apps and even to create your own robots