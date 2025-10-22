# 3b.CREATION FOR CHAT USING TCP SOCKETS
```
NAME: THEJASHREE S
REGNO: 212224240175
```
## AIM
To write a python program for creating Chat using TCP Sockets Links.
## ALGORITHM:
1. Import the necessary modules in python
2. Create a socket connection to using the socket module.
3. Send message to the client and receive the message from the client using the Socket module in
 server
4. Send and receive the message using the send function in socket.
## PROGRAM
Client:
```python
import socket 
s=socket.socket() 
s.connect(('localhost',8000)) 
while True: 
    msg=input("Client > ") 
    s.send(msg.encode()) 
    print("Server > ",s.recv(1024).decode())
```
Server:
```python
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
## OUTPUT
Client:

<img width="752" height="355" alt="image" src="https://github.com/user-attachments/assets/6298fbeb-4574-4fb7-8d30-e77cbaa08ed7" />

Server:

<img width="752" height="355" alt="image" src="https://github.com/user-attachments/assets/004dfa5e-228d-40ff-9f0c-cb16ff215a21" />

## RESULT
Thus, the python program for creating Chat using TCP Sockets Links was successfully 
created and executed.
