# ConcurrentCacheProxy

## Overview

This project implements a Multi-Threaded HTTP Proxy Server in C, which supports the caching of responses to optimize performance. The server can handle multiple client requests concurrently using threads with a caching mechanism to store responses for faster retrieval.

## Features

- **Multi-threaded Handling**: Each client request is managed in a separate thread, allowing concurrent processing of multiple requests.
- **Caching**: Responses from remote servers are cached to minimize redundant network traffic and improve response times.
- **Error Handling**: The proxy server responds with appropriate HTTP error messages (400, 403, 404, etc.) based on request validity.
- **HTTP Request Parsing**: Requests are parsed to extract essential information such as method, host, path, and HTTP version.

## Requirements

- GCC (GNU Compiler Collection) <br>
- pthread library for multi-threading support <br>
- POSIX-compliant system (Linux or macOS) <br>

## Installation

1. **Clone the Repository**:
   ```bash
   git clone <repository-url>
   cd <repository-directory>
   
2. **Compile the Proxy Server**: Use the provided Makefile to compile the server.
   ```bash
   make
   
3. **Run the Proxy Server**:
   ```bash
   Copy code
  ./proxy <port_number>

  ---> Replace <port_number> with the desired port for the proxy server (default is 8080).
  
## Usage

1. Configure your browser or HTTP client to use the proxy server's IP address and port.
2. Send HTTP GET requests through the proxy, and it will forward the requests to the specified servers.

## File Structure
. <br>
├── README.md              # Project documentation <br>
├── Makefile               # Build instructions <br>
├── proxy_server_with_cache.c  # Main server implementation <br>
├── proxy_parse.c          # HTTP request parsing and caching logic <br>
└── proxy_parse.h          # Header file for parsing functions and cache structure <br>

## Key Functions

handle_request(): Manages the client's request, checking the cache and forwarding the request if necessary. <br>
add_cache_element(): Adds a response to the cache. <br>
find(): Searches for a URL in the cache and updates its access time. <br>
remove_cache_element(): Removes the least recently used cache element when the cache exceeds its size limit. <br>

## Error Handling

**The proxy server implements various HTTP status codes**:

400 Bad Request: Invalid request format. <br>
403 Forbidden: Access denied to the requested resource. <br>
404 Not Found: The requested resource could not be found. <br>
500 Internal Server Error: Server encountered an unexpected condition. <br>

## Cleanup
To remove compiled files, use:
   ```bash
   make clean
   ```
To create a tarball of the project:
```bash
make tar
```
 ## Acknowledgments
 
>< Inspired by various networking and concurrent programming resources. <br>
>< Utilized the pthread library for multi-threading capabilities. <br>

## Contributing

Contributions are encouraged! Please follow these steps to contribute:

I. Fork the repository: git checkout -b feature/YourFeature <br>
II.Make your changes and commit: git commit -m "Add your feature" <br>
III. Push to the branch: git push origin feature/YourFeature <br>
IV. Create a pull request. <br>

Feel free to reach out for any questions or collaborations!

## Developer

This project is developed by ***Shobhit Singh***
