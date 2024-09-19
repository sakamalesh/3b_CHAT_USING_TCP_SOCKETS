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
## Server:
'''

    import socket
    s=socket.socket()
    s.connect(('localhost',8000))
    while True:
        msg=input("Client>")
        s.send(msg.encode())
        print("Server>",s.recv(1024).decode())

'''
## Client:
'''


    import socket
    s=socket.socket()
    s.bind(('localhost',8000))
    s.listen(5)
    c,addr=s.accept()
    while True:
        ClientMessage=c.recv(1024).decode()
        print("Client>",ClientMessage)
        msg=input("Server>")
        c.send(msg.encode())
'''
## OUPUT
![Screenshot 2024-09-19 105017](https://github.com/user-attachments/assets/3e0cf63f-50ff-4493-85f2-a4ad731eedb9)
![Screenshot 2024-09-19 105009](https://github.com/user-attachments/assets/0c4b77f5-d1ef-495b-9fa1-1d37e1a81b10)

## RESULT
Thus, the python program for creating Chat using TCP Sockets Links was successfully 
created and executed.
