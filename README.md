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
### SERVER:
```py
import socket
s=socket.socket()
s.connect(('localhost',8000))
while True:
 msg=input("Client > ")
 s.send(msg.encode())
 print("Server > ",s.recv(1024).decode())
```
### CLIENT:
```py
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
### SERVER:
![322287139-e0650656-4d5f-4eb5-b6ce-70fa2b9c8155](https://github.com/Sabariakash22009103/3b_CHAT_USING_TCP_SOCKETS/assets/119390227/efee9a01-05cb-4fcc-9852-f13faf39ac2b)
### CLIENT:
![322287152-dd8296af-dae4-41f6-bd40-5641a21f1257](https://github.com/Sabariakash22009103/3b_CHAT_USING_TCP_SOCKETS/assets/119390227/9e47d9f5-edbf-4882-a9f1-bc2c3b53e816)
## RESULT
Thus, the python program for creating Chat using TCP Sockets Links was successfully 
created and executed.
