# Unhandled Promise Rejection in Express.js

This repository demonstrates a common error in Express.js applications: unhandled promise rejections within request handlers.  When an asynchronous operation inside a route handler throws an error and isn't properly caught, the server will crash without returning a proper response to the client.  This example shows the issue and provides a solution.

## Bug

The `bug.js` file contains an Express.js server with a route handler that performs an asynchronous operation.  This operation is designed to throw an error. Because the error isn't handled properly within the `.then().catch()` block, the server crashes.

## Solution

The `bugSolution.js` file demonstrates how to correctly handle the error. The key is to ensure that the `.catch()` block appropriately handles the potential errors from the asynchronous operation and sends a suitable response to the client, preventing the server from crashing.