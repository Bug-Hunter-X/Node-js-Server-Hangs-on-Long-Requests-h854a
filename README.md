# Node.js Server Hang on Long Requests

This repository demonstrates a common issue in Node.js servers: hanging on long-running requests.  The provided code simulates a long-running task within the request handler, blocking the event loop and preventing the server from responding to subsequent requests.

The solution demonstrates the use of asynchronous operations and proper request handling to prevent the server from hanging.

## Bug

The `server.js` file contains the buggy code. Running this server and making a request will cause the server to hang for approximately 5 seconds before responding.  During this time, the server cannot handle any other requests. 

## Solution

The `serverSolution.js` file shows how to correctly handle long-running tasks using asynchronous techniques like `setTimeout` or Promises.  This prevents blocking the event loop and keeps the server responsive.