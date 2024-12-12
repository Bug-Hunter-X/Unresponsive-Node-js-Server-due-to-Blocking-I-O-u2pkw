# Unresponsive Node.js Server due to Blocking I/O

This repository demonstrates a common issue in Node.js where a long-running operation in the request handler blocks the event loop, making the server unresponsive.  The solution showcases how to use asynchronous operations to prevent this.

## Bug

The `bug.js` file contains a Node.js server that simulates a long-running operation (5 seconds) within the request handler. During this time, the server cannot process any other requests, leading to unresponsiveness.

## Solution

The `bugSolution.js` file demonstrates how to fix this by using asynchronous operations (timers or promises) that do not block the event loop.  This ensures the server remains responsive while handling requests.