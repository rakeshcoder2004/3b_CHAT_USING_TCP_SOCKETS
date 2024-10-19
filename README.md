
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
#### DEVELOPED BY: Rakesh V
#### REGISTER NO:21222110036
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
![image](https://github.com/user-attachments/assets/1c65f66c-94bf-49ac-b7cc-f89c170980d9)

### CLIENT:
![image](https://github.com/user-attachments/assets/190b8dc0-b995-4fa3-b5b7-9779ab910d9e)

## RESULT
Thus, the python program for creating Chat using TCP Sockets Links was successfully 
created and executed.
