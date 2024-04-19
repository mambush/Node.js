# Node.js
## WEEK 1
An open source server environment called Node.js On the server, JavaScript is used. A Node.js program doesn't create a new thread for every request; instead, it operates inside a single process. Asynchronous I/O primitives are built into the standard library of Node.js, preventing blocking in JavaScript code, and libraries in Node.js are generally developed with non-blocking paradigms. As a result, blocking behavior becomes the exception rather than the rule.
The most recent version of Node.js is v20.9, and it was created by Ryan Dahi in 2009. It is easily operable on Windows, Linux, Unix, macOS, and other platforms due to its cross-platform nature.
One special benefit of Node.js is that it doesn't need learning a new language to create server-side code—millions of frontend developers who write JavaScript for the browser can now write server-side code. One of the most well-liked options for creating web applications, microservices, and RESTful APIs is Node.js.

var http = require('http');

http.createServer(function (req, res) {
  res.writeHead(200, {'Content-Type': 'text/plain'});
  res.end('Welcome to GeeksforGeeks Node.js Tutorial');
}).listen(8080);
Explanation:

To run this Node.js code, save it as a server.js file and run “node server.js" in your terminal.
The server is set to listen on the specified port(8080) and host name(http://localhost:8080). When the server is ready, the callback function is called, in this case informing us that the server is running.
important Node.js features include:

JavaScript Everywhere: With Node.js, developers can leverage JavaScript from front-end to back-end of the application stack. Development is made easier by this uniformity, which also minimizes context change.
Asynchronous Programming Model: The I/O model used by Node.js is event-driven and non-blocking, or asynchronous. This makes it possible to handle several requests at once without preventing the completion of other operations. Node.js apps are therefore incredibly responsive and effective.
Quick Execution: Node.js makes use of Google's V8 engine, which assembles and runs JavaScript very quickly. It is appropriate for microservices and real-time applications because to its performance advantage.
Huge and Active Community: The Node.js framework boasts a thriving developer, library, and tool community. To improve your learning process, there are a ton of tools, tutorials, and help available.
Scalability: Due to its lightweight design and scalable nature, Node.js
Node.js is an open source, a server-side script which runs on the top of Google’s open-source scripting engine V8. Node.js is fast, lightweight and efficient. It uses the asynchronous mode of operation, event-driven Input/Output rather than using the traditional threads or separate threads for each process. Node.js was originally written by Ryan Dahl in the year 2009. It is a cross-platform Javascript run-time environment that executes Javascript code outside of a browser. Node.js uses javascript for creating node applications or we can use any other language that ultimately compiles to javascript (like typescript). The javascript is written in the same way as we’d use in any client-side application. However, we need to set up the node development environment.

Node.js is the greatest tool for building real-time web applications. It provides cross-platform applications which run easily on any web. So you basically don’t need anything extra for running up a node application. You only need for making one. According to the Node.js Survey of users, 43% of Node.js programmers claim to use Node.js for enterprise apps. It’s a light, scalable and open-source language platform which makes it very easy to build apps even at the enterprise level also. Overall it increases the efficiency of the development process as it fills the gap between frontend and backend applications. It uses the approach of non-blocking I/O. In Non-blocking I/O approach, you can initiate a request in parallel for user2 without waiting for the response to the request for user1. The requests in Node.js can initiate in parallel. This non-blocking I/O eliminates the need for multi-threading.

Npm (Node Package Manager)
These are the libraries which are built by the awesome community which will solve almost all the generic problems related to the Node.js. Npm has packages which are used in our apps to make the development process faster and more efficient.

Node Modules
Node.js has a set of built-in modules which can be used without any further installation. We can install some custom modules from the NPM as per the need of the application. We can also create modules of our own and use them by importing it in our apps. Basically, the Node module is a block of code which can be used again in any node.js component without impacting any other node.js component. The modules in node.js work independently without impacting the existence of any other functions.
NPM (Node Package Manager) is the default package manager for Node and is written entirely in JavaScript. Developed by Isaac Z. Schlueter, it was initially released in January 12, 2010. NPM manages all the packages and modules for Node and consists of command line client npm.

NPM gets installed into the system with installation of Node. The required packages and modules in Node project are installed using NPM. A package contains all the files needed for a module and modules are the JavaScript libraries that can be included in Node project according to the requirement of the project.

NPM can install all the dependencies of a project through the package.json file. It can also update and uninstall packages. In the package.json file, each dependency can specify a range of valid versions using the semantic versioning scheme, allowing developers to auto-update their packages while at the same time avoiding unwanted breaking changes.

Modules for Node.js

Modules are the enclosed code blocks in Node.js that interact with an external application based on the functionalities that are relevant to them. Modules might consist of a single file or a group of related files or folders. Because modules are reusable and can divide a complex piece of code into smaller, more manageable portions, programmers rely heavily on them. 

There are three kinds of modules:

Local Modules
Modules from third parties
## Core Modules: 
> When you install Node.js, you'll get access to a number of built-in modules that are part of the platform. By utilizing the necessary function, these modules can be imported into the application.
syntax:
const module = require('module_name');

const http = require('http');
http.createServer(function (req, res) {
	res.writeHead(200, { 'Content-Type': 'text/html' });
	res.write('Welcome to this page!');
	res.end();
}).listen(3000);
>In the above example, the require() function returns an object because the Http module returns its functionality as an object. The function http.createServer() method will be executed when someone tries to access the computer on port 3000. The res.writeHead() method is the status code where 200 means it is OK, while the second argument is an object containing the response headers. The following list contains some of the important core modules in Node.js
- Local Modules: Unlike built-in and external modules, local modules are created locally in your Node.js application. Let’s create a simple calculating module that calculates various operations. Create a calc.js file that has the following code:
  exports.add = function (x, y) {
	return x + y;
};

exports.sub = function (x, y) {
	return x - y;
};

exports.mult = function (x, y) {
	return x * y;
};

exports.div = function (x, y) {
	return x / y;
};
> Since this file provides attributes to the outer world via exports, another file can use its exported functionality using the require() function
const calculator = require('./calc');

let x = 50, y = 10;

console.log("Addition of 50 and 10 is "
			+ calculator.add(x, y));

console.log("Subtraction of 50 and 10 is "
			+ calculator.sub(x, y));

console.log("Multiplication of 50 and 10 is "
			+ calculator.mult(x, y));

console.log("Division of 50 and 10 is "
			+ calculator.div(x, y));
