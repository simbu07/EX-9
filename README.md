## EX-9 APPLICATION USING TCP SOCKETS - CREATING FOR CHAT CLIENT-SERVER
### DATE :03-05-2023

### AIM :
To write a python program for creating Chat using TCP Sockets Links.

### ALGORITHM :
```
1.Import the necessary modules in python
2.Create a socket connection to using the socket module.
3.Send message to the client and receive the message from the client using the Socket module in server
4.Send and receive the message using the send function in socket.
```
### PROGRAM :
```
Developed By: Silambarasan K
Reg No:212221230101
```
### CLIENT :
```py
import socket
s=socket.socket()
s.connect(('localhost',8000))
while True:
    msg=input("Client > ")
    s.send(msg.encode())
    print("Server > ",s.recv(1024).decode())
```
### SERVER :
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
### OUTPUT :
### CLIENT :
![image](https://user-images.githubusercontent.com/113497680/241549016-9b48ecc2-5897-4396-930a-126b68820c27.png)

### SERVER :
![image](https://user-images.githubusercontent.com/113497680/241549075-365ad1d9-9eea-495d-8679-1fd301dbf3c5.png)

### RESULT :
Thus, the python program for creating Chat using TCP Sockets Links was successfully created and executed.
