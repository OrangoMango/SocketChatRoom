# SocketChatRoom
Java socket chat room with TCP connection.  
Package: `com.orangomango.socket`

# How to use
## Quick setup
Clone the repository and change the directory to `bin`
```bash
git clone https://github.com/OrangoMango/SocketChatRoom
cd SocketChatRoom/bin
```
## Start server
There are 2 ways to start the server:
* run `java com.orangomango.socket.Server` and you will start a server with default values (port=1234)
* run `java com.orangomango.socket.Server <port>` and you will start a server with the specified port
## Connect a client
You can connect a client, either from another device in the same LAN or from the same device using another terminal
There are 2 ways to run a client:
* run `com.orangomango.socket.Client` and you will use a client with default values (host=localhost and port=1234)
* run `com.orangomango.socket.Client <host> <port>` and you will use a client with the specified values

# Start typing
## Client
From the client side you can simply write text and it will be sent to the other connected clients and the server.  
Use <Kbd>Ctrl+C</Kbd> to disconnect.  
Each client can use the following commands:
* `/list` to get the current connected users
* `@<username> msg` to privatly send a message to `username`. Message will be sent to the destinator AND the server.   
  Example: `@John hello`
## Server
In the server console you will get messages when someone connects/disconnects or someone writes something.  
Use <Kbd>Ctrl+C</Kbd> to close the server and disconnect all clients.  
You can also use the following commands to moderate the chat:
* `/kick <username>` Kick the specified username from server session. They can still rejoin.
* `/say <username> <message>` Send a private `message` to `username`.
* `/ban <username>` Ban the specified username. They cannot rejoin anymore untill they are unbanned.
* `/unban <username>` Unban the specified username.
* `/banlist` View current banlist
* `/list` List connected users
