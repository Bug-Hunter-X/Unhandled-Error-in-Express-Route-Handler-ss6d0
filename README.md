# Express.js Route Handler Error

This repository demonstrates a common error in Express.js route handlers:  lack of error handling for invalid input. The `bug.js` file contains code that is vulnerable to crashing if a non-numeric user ID is provided.  The `bugSolution.js` provides a corrected version with robust error handling.

## Bug
The bug lies in the `/users/:id` route. It attempts to parse the `id` parameter as an integer without handling the case where the parameter is not a valid integer. This will cause a runtime error if a non-numeric ID is passed.

## Solution
The solution includes explicit error checking and handling of invalid input.  It checks if the `userId` can be parsed as an integer and if the user exists before sending a response.  This prevents unexpected crashes and provides appropriate error messages to the client.