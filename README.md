# Node.js Server Unresponsiveness

This repository demonstrates a common Node.js issue where a long-running synchronous operation blocks the event loop, causing the server to become unresponsive to new requests.  The `blockingServer.js` file shows the problematic code, while `nonBlockingServer.js` provides a solution using asynchronous operations.

## Problem

The `blockingServer.js` example uses a `while` loop to simulate a 5-second CPU-bound task. During this time, the event loop is blocked, and the server cannot handle any other requests. This leads to unresponsiveness and poor performance.

## Solution

The `nonBlockingServer.js` example demonstrates how to avoid blocking the event loop by using asynchronous operations.  While not applicable in all cases, this pattern is crucial for maintaining responsiveness in Node.js applications.