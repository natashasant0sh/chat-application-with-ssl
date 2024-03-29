# Secure Chat Application
The Secure Chatroom Application is a multi-threaded, secure chatroom application with a client-server architecture, enabling users to communicate securely over SSL/TLS connections.

## Features
-Secure communication using OpenSSL for SSL/TLS encryption
-Multi-threaded server to handle multiple clients concurrently
-Client-server architecture using TCP/IP sockets
-User authentication with unique usernames
-Broadcast messages to all online users
-Private messaging between individual users
-Display a list of currently online users
-User-friendly command-line interface

## Technologies Used
-C programming language
-OpenSSL library for SSL/TLS encryption
-POSIX threads (Pthreads) for multi-threading
-TCP/IP sockets for network communication

## Getting Started
1. Clone the repository
2. Compile the server and client programs
   gcc -o server server.c helper.c -lpthread -lssl -lcrypto
   gcc -o client client.c helper.c -lpthread -lssl -lcrypto
3. Run the server
   ./server <port number>
4. Run the client
   ./client -a <server-ip> -p <port> -u <username>

## Usage
The client application accepts the following command-line arguments:
-h: Print help
-a <server-ip>: IP address of the server (required)
-p <port>: Port number of the server (required)
-u <username>: Your desired username (required)

Once connected to the server, the following commands are available:
msg "<message>": Send a message to all online users
msg "<message>" <username>: Send a private message to a specific user
online: Display a list of currently online users
help: Show the available commands
quit: Exit the chatroom
