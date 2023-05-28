# EX-9 APPLICATION USING TCP SOCKETS - CREATING FOR CHAT CLIENT-SERVER

# DATE : 
04-05-2023

# AIM :
To write a python program for creating Chat using TCP Sockets Links

# ALGORITHM :
1.Start the program.

2.Get the frame size from the user. To create the frame based on the user request. 

3.To send frames to server from the client side. 

4.If your frames reach the server, it will send ACK signal to client otherwise it will sendNACK signal to client. 

5.Stop the program

# PROGRAM :
# CLIENT:
```
import socket
s=socket.socket()
s.connect(('localhost',8000))
while True:
    msg=input("Client > ")
    s.send(msg.encode())
    print("Server > ",s.recv(1024).decode())
  ```
# SERVER:
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
# OUTPUT :

![image](https://github.com/ieswaris/EX-9/assets/127847210/041f8fad-82e3-47f6-a9be-a5e153359002)

# RESULT :
Thus, the python program for creating Chat using TCP Sockets Links was successfully created and executed.
