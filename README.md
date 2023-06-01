# EX-9 APPLICATION USING TCP SOCKETS - CREATING FOR CHAT CLIENT-SERVER

## DATE : 02/05/2023

## AIM :
To write a python program for creating Chat using TCP Sockets Links.

## ALGORITHM :

1.Import the necessary modules in python

2.Create a socket connection to using the socket module.

3.Send message to the client and receive the message from the client using the Socket module in server

4.Send and receive the message using the send function in socket.

## PROGRAM :
## client :
Developed by : yogesh rao S D
Register no : 212222110055
```
import socket
s=socket.socket()
s.connect(('localhost',8000))
while True:
 msg=input("Client > ")
 s.send(msg.encode())
 print("Server > ",s.recv(1024).decode())
 ```
## server :
Developed by : yogesh rao S D
Register no : 212222110055
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
## OUTPUT :

## clientoutput :

![6 client](https://github.com/yogeshrao05/EX-9/assets/122008288/9e57dddc-7bca-4e77-ae49-cf664b17b11a)


## serveroutput :

![6server](https://github.com/yogeshrao05/EX-9/assets/122008288/58520192-f5c0-4f70-bc97-5ccab3d2f747)


## RESULT :
Thus, the python program for creating Chat using TCP Sockets Links was successfully created and executed
