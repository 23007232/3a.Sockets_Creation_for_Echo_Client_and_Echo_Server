# 3a.CREATION FOR ECHO CLIENT AND ECHO SERVER USING TCP SOCKETS
```
Name:Pavithra P
Reg No:212223110035
```
# AIM
To write a python program for creating Echo Client and Echo Server using TCP
Sockets Links.
## ALGORITHM:
1. Import the necessary modules in python
2. Create a socket connection to using the socket module.
3. Send message to the client and receive the message from the client using the Socket module in
 server .
4. Send and receive the message using the send function in socket.
## PROGRAM
 CLIENT:
```
import socket
s=socket.socket()
s.connect(('localhost',8000))
while True:
 msg=input("Client > ")
 s.send(msg.encode())
 print("Server > ",s.recv(1024).decode())
```
SERVER:
```
import socket
s=socket.socket()
s.bind(('localhost',8000))
s.listen(5)
c,addr=s.accept()
while True:
 ClientMessage=c.recv(1024).decode()
 c.send(ClientMessage.encode())
```
## OUPUT
### CLIENT:
![image](https://github.com/23007232/3a.Sockets_Creation_for_Echo_Client_and_Echo_Server/assets/139115574/d177b217-bcfa-45bb-a1d9-2371db2e6217)
### SERVER:
![image](https://github.com/23007232/3a.Sockets_Creation_for_Echo_Client_and_Echo_Server/assets/139115574/9c9ca219-8e25-40d8-a7c6-7f4b0ffc228d)

## RESULT
Thus, the python program for creating Echo Client and Echo Server using TCP Sockets Links 
was successfully created and executed.
