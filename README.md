# Express.js Route Handler: Missing Error Handling for Invalid User IDs

This repository demonstrates a common error in Express.js route handlers: missing error handling for invalid input.  Specifically, the route `/users/:id` attempts to parse the `id` parameter as an integer without checking for potential errors. This can lead to unexpected behavior or crashes if a non-numeric ID is provided.

## Bug

The `bug.js` file contains the erroneous code.  It attempts to find a user based on their ID, but fails to handle the case where the ID is not a valid number.  This may result in a runtime error or an unexpected response.

## Solution

The `bugSolution.js` file demonstrates how to properly handle this situation by adding error handling for invalid input.  The solution checks if the ID is a valid number before attempting to parse it. If it's not a number, it sends an appropriate error response.  This prevents crashes and ensures a more robust application.

## How to Run

1. Clone this repository.
2. Install dependencies using `npm install`.
3. Run the `bug.js` (to see the error) or `bugSolution.js` (to see the solution).