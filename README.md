# EX-9 APPLICATION USING TCP SOCKETS - CREATING FOR CHAT CLIENT-SERVER

## DATE : 02-05-2023

## AIM :
To write a python program for creating Chat using TCP Sockets Links.

## ALGORITHM :
1. Start the program.
2. Get the frame size from the user.
3. To create the frame based on the user request.
4. To send frames to server from the client side.
5. If your frames reach the server, it will send ACK signal to client otherwise it
will sendNACK signal to client.
6. Stop the program .


## PROGRAM :
### CLIENT :
```
import socket
s=socket.socket()
s.connect(('localhost',8000))
while True:
   msg=input("Client > ")
   s.send(msg.encode())
   print("Server > ",s.recv(1024).decode())
  ```
### SERVER :
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
### CLIENT :

![241381313-99e374d6-1340-4373-8763-15abc9afc439](https://github.com/Mena-Rossini/EX-9/assets/102855266/8c68967e-3c5d-458a-888a-87c5ef799c43)

### SERVER :
![241381327-c95b5a97-cf96-4e90-9bd5-22fdc7b3aa3b](https://github.com/Mena-Rossini/EX-9/assets/102855266/af296742-f546-48bd-868e-bfaf2729189e)

## RESULT :
Thus, the python program for creating Chat using TCP Sockets Links was successfully 
created and executed . 
