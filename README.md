# 3b.CREATION FOR CHAT USING TCP SOCKETS
## AIM
To write a python program for creating Chat using TCP Sockets Links.
## ALGORITHM:
1. Import the necessary modules in python
2. Create a socket connection to using the socket module.
3. Send message to the client and receive the message from the client using the Socket module in
 server
4. Send and receive the message using the send function in socket.
## PROGRAM
## CLIENT:
```
NAME: M THEJESWARAN
REG NO:212223240168

import socket 
s=socket.socket() 
s.connect(('localhost',8000)) 
while True: 
    msg=input("Client > ") 
    s.send(msg.encode()) 
    print("Server > ",s.recv(1024).decode())
```

## SERVER:
```
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

## OUPUT
## CLIENT
![image](https://github.com/user-attachments/assets/85b9a40a-32a9-46eb-9e9c-cd630f6c046e)

## SERVER
![image](https://github.com/user-attachments/assets/b7b61e68-3bab-44f6-a64d-cd6f2cd17829)

## RESULT
Thus, the python program for creating Chat using TCP Sockets Links was successfully 
created and executed.
