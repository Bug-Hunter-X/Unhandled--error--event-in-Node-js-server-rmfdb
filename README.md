# Unhandled 'error' event in Node.js Server

This repository demonstrates a common yet easily missed error in Node.js: unhandled exceptions within HTTP request handlers.  The server crashes silently without providing helpful debugging information.

## The Problem

The `bug.js` file shows a simple Node.js HTTP server.  However, it lacks proper error handling. If an unexpected error occurs during request processing (e.g., parsing invalid JSON), the server will crash without informative logs.

## The Solution

`bugSolution.js` provides a corrected version.  It adds comprehensive error handling using `try...catch` blocks and logs errors to the console. This allows for better debugging and prevents unexpected server crashes.  It also gracefully handles bad requests.