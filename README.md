# Express.js Route Handler Error: Missing Error Handling

This repository demonstrates a common error in Express.js route handlers: the lack of error handling for invalid input. The example shows a route that fetches a user by ID.  If the ID is not a number, the code will throw an error.  The solution shows how to add proper error handling to gracefully manage such scenarios.

## Bug

The `bug.js` file contains the buggy code.  It attempts to parse the user ID as an integer without checking for potential errors.  If a non-numeric ID is passed, the `parseInt` function will return `NaN`, leading to a `Cannot read properties of undefined (reading 'id')` error. 

## Solution

The `bugSolution.js` file demonstrates the corrected code. It includes comprehensive error handling to check if the ID is a valid number and handles the case where the user is not found.