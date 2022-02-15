# Whatsapp!

This is a python script to imitate Whatsapp! Each user can send broadcast messages to all other users connected to the server. Or send specific messages to a specific user. Each user may follow a list of words that if any of those are included in a message sent by anyone, he will receive the message. This program uses python sockets and handles events. Attaching is another feature of this app. Each user may attach a file and send it to a specific user.

## Setup
1. Run server.py script:
```
python3 server.py
```
2. Read the message in server side and use the port number allocated by the server to run the client (specify the username of the client in <username>):
```
python3 client.py <username> chat://localhost:<port>
```
## Features
1. The server randomly picks a port available in its device.
2. Each client communicate using a distinct TCP connection. Server handles numerous clients at the same time.
3. There are a list of control messages such as:
   1. gfd
4. 
