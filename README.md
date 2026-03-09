# 3b.CREATION FOR CHAT USING TCP SOCKETS
## AIM
To write a python program for creating Chat using TCP Sockets Links.
## ALGORITHM:
1. Import the necessary modules in python
2. Create a socket connection to using the socket module.
3. Send message to the client and receive the message from the client using the Socket module in
 server
4. Send and receive the message using the send function in socket.
## PROGRAM:
## Server:
```
server.py
import socket 
s=socket.socket() 
s.bind(('localhost',8000)) 
s.listen(5) 
c,addr=s.accept() 
while True: 
            ClientMessage=c.recv(1024).decode() 
            print("Client > ",ClientMessage) 
            msg=input("Server > ") 
            c.send(msg.encode())
```
## Client:
```
client.py
import socket 
s=socket.socket() 
s.connect(('localhost',8000)) 
while True: 
    msg=input("Client > ") 
    s.send(msg.encode()) 
    print("Server > ",s.recv(1024).decode())
```
## OUPUT:
## Server:
<img width="1484" height="261" alt="image" src="https://github.com/user-attachments/assets/d64c13dc-46f6-4c66-bd07-178c55f1177a" />

## Client:
<img width="1482" height="288" alt="image" src="https://github.com/user-attachments/assets/307f4fdf-4dc4-462b-93b2-0c8e4c7b4f4c" />


## RESULT
Thus, the python program for creating Chat using TCP Sockets Links was successfully 
created and executed.
