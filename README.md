<H1 ALIGN=CENTER> CREATION OF CHAT USING TCP SOCKETS </H1>
<H3> NAME : SHRRUTHILAYA G </H3>
<H3> REGISTER NUMBER : 212221230097 </H3>
<H3>EXPERIMENT NO : 03 B </H3>
<H3>DATE  : 11.05.2024 </H3>

## AIM:
To write a python program for creating Chat using TCP Sockets Links.
## PROCEDURE:
1. Import the necessary modules in python
2. Create a socket connection to using the socket module.
3. Send message to the client and receive the message from the client using the Socket module in
 server
4. Send and receive the message using the send function in socket.

## PROGRAM:
### CLIENT:
```PYTHON
import socket
s = socket.socket()
s.connect(('localhost',8000))
while True:
    msg = input("Client > ")
    s.send(msg.encode())
    print("Server > ", s.recv(1024).decode())
```
### SERVER:

```PYTHON
import socket
s = socket.socket()
s.bind(('localhost',8000))
s.listen(5)
c, addr = s.accept()
while True:
    ClientMessage = c.recv(1024).decode()
    print("Client > ", ClientMessage)
    msg = input("Server > ")
    c.send(msg.encode())
```
## OUTPUT:
### CLIENT:
![client](https://github.com/Shrruthilaya-Gangadaran/3b_CHAT_USING_TCP_SOCKETS/assets/93427705/ce82aa35-07ba-4137-8a00-3221446b129f)

### SERVER:

![server](https://github.com/Shrruthilaya-Gangadaran/3b_CHAT_USING_TCP_SOCKETS/assets/93427705/eb91ca2c-551d-42f4-b2e5-e51a61492d9f)

## RESULT:
Thus, the python program for creating Chat using TCP Sockets Links was successfully 
created and executed.
