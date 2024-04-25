# 2a_Stop_and_Wait_Protocol
# Name :Iswarya P
# Reg no:212223230082
## AIM 
To write a python program to perform stop and wait protocol
## ALGORITHM
1. Start the program.
2. Get the frame size from the user
3. To create the frame based on the user request.
4. To send frames to server from the client side.
5. If your frames reach the server it will send ACK signal to client
6. Stop the Program
## PROGRAM
## Client-Side
```
import socket
s=socket.socket()
s.bind(('localhost',8000))
s.listen(5)
c,addr=s.accept()
while True:
 i=input("Enter a data: ")
 c.send(i.encode())
 ack=c.recv(1024).decode()
 if ack:
 print(ack)
 continue
 else:
 c.close()
 break
```

## Server-Side
```
import socket
s=socket.socket()
s.connect(('localhost',8000))
while True:
 print(s.recv(1024).decode())
 s.send("Acknowledgement Recived".encode())
```

## OUTPUT
![wk8wu21f](https://github.com/Iswarya0580/2a_Stop_and_Wait_Protocol/assets/149989171/5c4fc40b-3735-453b-b5a1-76fa963c80b1)


## RESULT
Thus, python program to perform stop and wait protocol was successfully executed.
