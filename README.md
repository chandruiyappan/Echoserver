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

```
Name:Kavi Keerthana R
Reg No:212222100022
```

## Server:
```
import socket


HOST = "127.0.0.1"  # Standard loopback interface address (localhost)
PORT = 65432  # Port to listen on (non-privileged ports are > 1023)


with socket.socket(socket.AF_INET, socket.SOCK_STREAM) as s:
    s.bind((HOST, PORT))
    s.listen()
    conn, addr = s.accept()
    with conn:
        print(f"Connected by {addr}")
        while True:
            data = conn.recv(1024)
            if not data:
                break
            conn.sendall(data)
```

## Client:
```
import socket


HOST = "127.0.0.1"  # The server's hostname or IP address
PORT = 65432  # The port used by the server


with socket.socket(socket.AF_INET, socket.SOCK_STREAM) as s:
    s.connect((HOST, PORT))
    s.sendall(b"KAVI KEERTHANA R-212222100022")
    data = s.recv(1024)


print(f"Received {data!r}")
```
## OUTPUT:
## Server:
![Screenshot 2024-09-11 192722](https://github.com/user-attachments/assets/ff197928-277a-4b54-9f90-4b995820a983)

## Client:
![Screenshot 2024-09-11 192738](https://github.com/user-attachments/assets/6dee04a9-1f6b-42cb-9aaf-5aaa07725251)



## RESULT:
The program is executed successfully
