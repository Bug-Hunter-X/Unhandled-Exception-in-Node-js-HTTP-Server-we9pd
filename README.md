# Unhandled Exception in Node.js HTTP Server

This repository demonstrates a common error in Node.js where an unhandled exception within an HTTP server's request handler can lead to unexpected crashes.  The `bug.js` file shows the problematic code, while `bugSolution.js` presents a corrected version.

## Bug

The original code lacks proper error handling within the request handler.  If a runtime error occurs (like the `throw new Error` in the example), the server will terminate abruptly without providing useful information about the error.

## Solution

The solution involves implementing a robust `try...catch` block to handle potential errors within the request handler. This prevents server crashes and allows for more graceful error handling, logging, or alternative responses to the client.