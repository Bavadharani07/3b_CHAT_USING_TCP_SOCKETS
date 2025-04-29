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
<h2>Client</h2>

```
import socket
s=socket.socket()
s.connect(('localhost',8000))
while True:
    msg=input("Client > ")
    s.send(msg.encode())
    print("Server > ",s.recv(1024).decode())
```
<h2>Server</h2>

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

<h2>Client</h2>

![Screenshot 2025-04-29 230023](https://github.com/user-attachments/assets/58bf2b2e-c59f-44d1-a129-18f4ca910e20)

<h2>Server</h2>


![Screenshot 2025-04-29 230033](https://github.com/user-attachments/assets/06b781e4-b81a-48f1-8821-7b84b2e1f0c5)


## RESULT
Thus, the python program for creating Chat using TCP Sockets Links was successfully 
created and executed.
