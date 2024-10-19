# ConcurrentCacheProxy
A multi-threaded HTTP proxy server in C with dynamic caching for improved performance and response times.
# HTTP Proxy Server with Caching

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
