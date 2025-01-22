# Express.js Route Handler Missing Error Handling for Invalid User ID

This repository demonstrates a common error in Express.js route handlers: the lack of error handling for invalid input.  Specifically, the `/users/:id` route attempts to parse the `id` parameter as an integer, but does not handle cases where the parameter is not a valid integer. This can lead to unexpected behavior or application crashes.

## Bug
The `bug.js` file contains the erroneous code.  The route handler does not check if `req.params.id` can be successfully parsed as an integer, causing a potential `NaN` error if the input is not a number.

## Solution
The `bugSolution.js` file provides a corrected version of the code. It includes error handling to check if `req.params.id` is a valid number before attempting to parse it, making the route more robust and preventing unexpected behavior.