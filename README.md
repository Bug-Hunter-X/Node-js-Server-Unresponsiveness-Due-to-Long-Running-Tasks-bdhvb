# Node.js Server Unresponsiveness

This repository demonstrates a common issue in Node.js applications:  unresponsiveness caused by long-running operations blocking the event loop.  The `server.js` file contains a simple HTTP server that simulates a 5-second delay. During this delay, the server becomes unresponsive to new requests.

The `serverSolution.js` file provides a solution using asynchronous operations or worker threads to prevent blocking the event loop.

## How to Reproduce

1. Clone this repository.
2. Run `node server.js`.
3. Open multiple browser tabs to access `http://localhost:3000`. Observe the behavior when multiple requests are sent concurrently.

## Solution

The provided solution uses asynchronous programming to handle long-running tasks without blocking the event loop, ensuring the server remains responsive.