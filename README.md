# Unhandled Promise Rejection in Asynchronous Node.js Express App

This repository demonstrates a common error in Node.js applications: unhandled promise rejections or uncaught exceptions within asynchronous callbacks.  The `bug.js` file showcases this issue, while `bugSolution.js` provides a corrected version with proper error handling.

## The Problem

Asynchronous operations, especially those involving callbacks or promises, can be challenging to handle correctly in Node.js. Unhandled errors in these asynchronous flows can lead to unexpected crashes or silent failures.

## The Solution

The key to avoiding these issues is comprehensive error handling. This includes:

1. **Using `try...catch` blocks** to handle potential errors within asynchronous functions.
2. **Attaching an event listener for `unhandledRejection`** to catch promise rejections that escape your `try...catch` blocks.

## How to Run

1. Clone this repository.
2. Navigate to the directory.
3. Run `npm install express` to install the dependencies.
4. Run `node bug.js` to observe the error.
5. Run `node bugSolution.js` to see the fixed version.