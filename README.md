# EX-2 IMPLEMENTATION OF STOP AND WAIT PROTOCOL

# DATE:13/03/2023

# AIM :
To write a python program to perform stop and wait protocol



# ALGORITHM :

1. Start the program.
2. Get the frame size from the user
3. To create the frame based on the user request.
4. To send frames to server from the client side.
5. If your frames reach the server it will send ACK signal to client otherwise it
will send NACKsignal to client.
6. Stop the program


# PROGRAM :

# CLIENT PROGRAM:
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
# SERVER PROGRAM:
```
import socket
s=socket.socket()
s.connect(('localhost',8000))
while True:
print(s.recv(1024).decode())
s.send("Acknowledgement Recived".encode())


```
# OUTPUT :
# CLIENT OUTPUT:

![image](https://github.com/kasivishvanathV/EX-2/assets/118787417/28fbdb81-eaf5-4388-b082-e4c1db751536)


# SERVER OUTPUT:

![Screenshot (150)](https://github.com/kasivishvanathV/EX-2/assets/118787417/123769e7-1e29-43d9-acd8-decc4e02f468)





RESULT :
Thus, python program to perform stop and wait protocol was successfully executed.



