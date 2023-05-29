# Chat Program
This is a simple chat program implemented in C language. The program includes a chat server and client applications that can connect to the server to exchange messages.

## Overview
The chat program consists of two main components: the server and the client. The server accepts incoming client connections, maintains a list of connected clients, and relays messages between clients. Each message sent by a client is tagged with a timestamp and the name of the sender.

The client application allows users to connect to the server, send messages, and receive messages from other connected clients. The client program provides a simple command-line interface for interacting with the chat server.

##Instructions
Building the Program
Make sure you have a C compiler (e.g., GCC) installed on your system.

Download or clone the chat program source code from the repository.

Open a terminal and navigate to the directory where the source code is located.

Compile the server program using the following command:

##Copy code
gcc server.c -o server
Compile the client program using the following command:

##Copy code
gcc client.c -o client
Running the Program
Start the server by running the following command in a terminal:

bash
##Copy code
./server
The server will start and display a message indicating that it is running.

Open another terminal window and run the client program using the following command:

bash
Copy code
./client
The client program will prompt you to enter your name. Enter a name and press Enter.

You can now send messages by typing them in the client terminal and pressing Enter. The messages will be relayed to other connected clients.

To quit the client program, type "/quit" and press Enter.

To stop the server, go to the server terminal and press Ctrl+C.

##Implementation Details
The server program uses sockets to establish connections with clients and create a new thread for each client connection. It uses message passing to relay messages between clients. The server maintains a list of connected clients and manages access to shared resources using mutex locks.

The client program connects to the server using a socket and allows users to send and receive messages. It runs on a separate terminal window and provides a simple command-line interface.
