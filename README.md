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


# SERVER PROGRAM:

import socket
s=socket.socket()
s.connect(('localhost',8000))
while True:
print(s.recv(1024).decode())
s.send("Acknowledgement Recived".encode())



# OUTPUT :
# CLIENT OUTPUT:

![image](https://github.com/kasivishvanathV/EX-2/assets/118787417/7e739ea1-fe48-4e89-8e80-e9d992ed9f90)

# SERVER OUTPUT:

![image](https://github.com/kasivishvanathV/EX-2/assets/118787417/dc9d3dc0-2e44-4b4c-b12a-9df7284be60c)




RESULT :
Thus, python program to perform stop and wait protocol was successfully executed.



