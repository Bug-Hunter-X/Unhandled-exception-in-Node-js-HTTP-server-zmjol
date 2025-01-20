# Unhandled Exception in Node.js HTTP Server

This repository demonstrates an example of an unhandled exception in a Node.js HTTP server and how to properly handle it.

## Bug

The `bug.js` file contains an HTTP server that throws an exception if the request URL is `/error`.  The error is not properly caught, resulting in the server crashing.

## Solution

The `bugSolution.js` file demonstrates the correct way to handle exceptions. It uses a `try...catch` block to catch the error and prevents the server from crashing.  Error handling is essential for robust server-side applications.

## How to reproduce

1. Clone the repository.
2. Navigate to the directory.
3. Run `node bug.js`.
4. Access `http://localhost:3000` in your browser. It will show 'Hello world'.
5. Access `http://localhost:3000/error` in your browser. The server will crash.
6. Run `node bugSolution.js`.  Access both URLs; the server will handle the error gracefully.

## Lessons Learned

Always use `try...catch` blocks to handle potential errors in your Node.js applications, especially those involving I/O operations like HTTP requests.  Unhandled exceptions can lead to application instability and data loss.