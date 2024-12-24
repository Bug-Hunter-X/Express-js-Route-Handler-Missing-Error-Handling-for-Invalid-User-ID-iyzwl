# Express.js Route Handler Missing Error Handling for Invalid User ID

This repository demonstrates a common error in Express.js route handlers:  missing error handling for invalid input parameters.  Specifically, the provided code lacks error handling for a scenario where the user ID is not a valid integer.

## Bug

The `bug.js` file contains an Express.js route handler that fetches a user based on their ID.  It attempts to parse the ID as an integer but does not handle potential errors (e.g., if the ID is not a number, or if `users` is undefined).  This can lead to unexpected behavior or application crashes.

## Solution

The `bugSolution.js` file presents a corrected version of the route handler. It includes comprehensive error handling to gracefully manage invalid user IDs, ensuring the application remains stable and responsive in all cases.

## How to Reproduce

1. Clone this repository.
2. Navigate to the repository's directory.
3. Run `npm install express`
4. Run `node bug.js` (for the buggy version) or `node bugSolution.js` (for the corrected version).
5. Send a GET request to `/users/{id}` with a non-integer value of {id} to observe the different behaviors.