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
1.To list all users that are connected, each user may use the following command:
```
!list
```
This lists all connected users and their user names.
2. Each client have a follow list. He may add items to this following list (items might be usernames or any given word). To do this, each client may use the following command:
```
!follow <item>
```
or 
```
!follow @<username>
```
3. Each user may see all items he is already following:
```
!follow?
```
4. Each user may unfollow an item which is already in his following list. Client app checks for all exceptions that may take place and generates informative errors.
5. The client may send a message to all users by including @all in his message.
6. Each client may send a message to a specific user by adding @<username> in his message.
7. Each user may attach an image or any kind of file to its message and send it to an individual or all clients.
```
!attach file.zip @all @<username>
``` 
8.  The server randomly picks a port available in its device.
9.  Each client communicate using a distinct TCP connection. Server handles numerous clients at the same time.
