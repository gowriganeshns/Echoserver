# Echoserver
Echo server and client using python socket

# AIM:

To develop a simple webserver to serve html programming pages.

## DESIGN STEPS:

### Step 1:

Design of echo server and client using python socket

### Step 2:

Implementation using Python code

### Step 3:

Testing the server and client 

## PROGRAM:
server code:
```
import socket

s=socket.socket()

host=socket.gethostname()
port=1234

s.bind((host, port))

s.listen(5)

while True:
    conn, addr = s.accept()
    print("Got connection from :", addr)
    conn.send(b'Thank you for connecting')
    conn.close()
```
client code:
```
import socket

s=socket.socket()

host=socket.gethostname()
port=1234

s.connect((host,port))
print(s.recv(1024))
s.close()
```
## OUTPUT:
server output:
![Screenshot 2024-03-05 114353](https://github.com/gowriganeshns/Echoserver/assets/162027231/74454e6c-146d-426f-bff5-77366cc7501a)

client output:
![Screenshot 2024-03-05 114407](https://github.com/gowriganeshns/Echoserver/assets/162027231/5d70d40d-6a1e-4e30-8f53-383bfe9a3f64)


## RESULT:
The program is executed successfully
