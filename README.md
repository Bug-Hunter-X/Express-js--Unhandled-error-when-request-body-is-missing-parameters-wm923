# Express.js Unhandled Error: Missing Request Body Parameters

This repository demonstrates a common error in Express.js applications: unhandled errors when the request body is missing expected parameters.

## Bug Description

The `bug.js` file contains an Express.js application that handles POST requests to the `/user` endpoint.  It expects a `name` parameter in the request body. However, it lacks proper error handling for scenarios where the request body is missing or incomplete.

If a POST request is made without a `name` parameter, the application will throw an error, causing it to crash.  The bug demonstrates the importance of robust error handling for production-ready Express.js applications.

## Solution

The `bugSolution.js` file provides a corrected version with comprehensive error handling.  It checks if the request body is valid before accessing its parameters and handles potential errors gracefully, returning appropriate error responses to the client.

## How to reproduce the bug
1. Clone this repository.
2. Navigate to the directory `cd express-missing-param`. 
3. Run `npm install`
4. Run `node bug.js`
5. Send a POST request to `http://localhost:3000/user` with a missing 'name' parameter using a tool like Postman or curl.

## How to see the solution
1. Run `node bugSolution.js`
2. Send the same POST request again. 
3. The server should respond with a proper error message instead of crashing.