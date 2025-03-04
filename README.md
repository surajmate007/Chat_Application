# Chat_Application
This project implements Chat Application in Python
 
## Overview

This project implements a simple client-server messaging system using Python. It allows multiple clients to register with a server, send messages to specific users, and even broadcast messages to all registered users. The communication follows a structured format to ensure message integrity and error handling.

## Features

- **Client-Server Communication:** Uses a server to handle connections and message forwarding between clients.
- **User Registration:** Clients must register with the server before sending or receiving messages.
- **Message Forwarding:** Messages are first sent to the server, which checks the format before forwarding them to the recipient.
- **Broadcasting:** Clients can send messages to all registered users using the `ALL` keyword.
- **Error Handling:** The system includes various error messages for malformed usernames, unregistered users, message forwarding failures, and incomplete headers.

## Message Format

Clients send messages in the format:  
```
@[recipient_name]: [message_content]
```
The server forwards messages using:  
```
FORWARD [username] Content-length: [length] [message_content]
```

## Error Codes

- `ERROR 100`: Malformed username  
- `ERROR 101`: No user registered  
- `ERROR 102`: Unable to send  
- `ERROR 103`: Header incomplete  

## How to Run

1. Start the server:  
   ```
   python3 server.py
   ```
2. Start a client:  
   ```
   python3 client.py [username] [server_IP]
   ```
3. Clients can send messages using the predefined format.

## Future Improvements

- Implement message encryption for secure communication.
- Support for file transfers between users.
- Introduce a GUI-based client interface.


How to run this code:
1. First run the server.py file.
2. Run client.py file and give input in format python3 client.py [username] [IP address].
3. Then the server will automatically register the client for both sending and receiving port.
4. After registering multiple users one of the user which will behave like sender will put the name of the receiver to send the message. The format is like:                @[username]: [content of the message]
5. Once the message is created it will be sent by pressing the enter key. The message will reach to receivers terminal.

----***----        For further details, please refer to **Solution_Description.pdf** file.      ----***----

Thank You !
