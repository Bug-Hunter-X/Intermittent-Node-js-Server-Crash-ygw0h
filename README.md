# Intermittent Node.js Server Crash

This repository demonstrates a bug causing intermittent crashes in a simple Node.js HTTP server. The server runs without issue for some time, then unexpectedly exits without any apparent error messages in the console.

## Bug Description
The server, implemented using the built-in `http` module, seemingly handles requests correctly. However, after a period of operation it terminates without warning.  No errors are logged to the console.

## How to Reproduce
1. Clone the repository.
2. Run `node server.js`.
3. Send requests to the server (e.g., using `curl`).
4. Observe the server running for some time.  It will eventually crash.

## Solution
The solution involves improved error handling. The original code lacked any mechanism to catch and log unhandled exceptions or process events that could lead to server crashes.

## Contributing
Contributions are welcome! Feel free to open issues or submit pull requests.