# React Router Dom v6 Incorrect Route Matching with Nested Routes and Params

This repository demonstrates a subtle bug in React Router Dom v6 related to route matching when nested routes with parameters are involved. The issue occurs when a route with parameters is defined, and another route (or routes) is present that partially matches a subset of the path of the route with the parameter.  The nested route with the param may not render correctly or may not be matched at all depending on the order of the routes.  This example showcases the issue and provides a solution.

## How to Reproduce

1. Clone the repository.
2. Run `npm install`.
3. Run `npm start`.
4. Navigate to `/users/123`.  Notice that the User component does not render. This is the unexpected behavior that is showcased in this example.

## Solution

The solution involves careful ordering of routes to ensure that the most specific route is matched first. Refer to the `bugSolution.js` file to review the solution.