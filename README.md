# ConcurrentCacheProxy

## Overview

This project implements a multi-threaded HTTP proxy server in C, which supports caching of responses to optimize performance. The server can handle multiple client requests concurrently using threads, with a caching mechanism to store responses for faster retrieval.

## Features

- **Multi-threaded Handling**: Each client request is managed in a separate thread, allowing concurrent processing of multiple requests.
- **Caching**: Responses from remote servers are cached to minimize redundant network traffic and improve response times.
- **Error Handling**: The proxy server responds with appropriate HTTP error messages (400, 403, 404, etc.) based on request validity.
- **HTTP Request Parsing**: Requests are parsed to extract essential information such as method, host, path, and HTTP version.

## Requirements

- GCC (GNU Compiler Collection)
- pthread library for multi-threading support
- POSIX-compliant system (Linux or macOS)

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
Configure your browser or HTTP client to use the proxy server's IP address and port.
Send HTTP GET requests through the proxy, and it will handle forwarding the requests to the specified servers.

## File Structure
.
├── README.md              # Project documentation
├── Makefile               # Build instructions
├── proxy_server_with_cache.c  # Main server implementation
├── proxy_parse.c          # HTTP request parsing and caching logic
└── proxy_parse.h          # Header file for parsing functions and cache structure
