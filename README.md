# 4.Execution_of_NetworkCommands
## NAME:GOKUL S
## REF.NO:212223040051
## AIM :Use of Network commands in Real Time environment
## Software : Command Prompt And Network Protocol Analyzer
## Procedure: To do this EXPERIMENT- follows these steps:
<BR>
In this EXPERIMENT- students have to understand basic networking commands e.g cpdump, netstat, ifconfig, nslookup ,traceroute and also Capture ping and traceroute PDUs using a network protocol analyzer 
<BR>
All commands related to Network configuration which includes how to switch to privilege mode
<BR>
and normal mode and how to configure router interface and how to save this configuration to
<BR>
flash memory or permanent memory.
<BR>
This commands includes
<BR>
• Configuring the Router commands
<BR>
• General Commands to configure network
<BR>
• Privileged Mode commands of a router 
<BR>
• Router Processes & Statistics
<BR>
• IP Commands
<BR>
• Other IP Commands e.g. show ip route etc.
<BR>

## PING COMMAND
## AIM:
To write the python program for simulating ping command.
## ALGORITHM:
Step 1: start the program

Step 2: Include necessary package in java.

Step 3: To create a process object p to implement the ping command.

Step 4: declare one Buffered Reader stream class object.

Step 5: Get the details of the server

 5:1: length of the IP address.

  5:2: time required to get the details.
 
 5:3: send packets, receive packets and lost packets. 
 
 5.4: minimum, maximum and average times.

Step 6: print the results. 

Step 7: Stop the program.
## PROGRAM
### CLIENT
~~~ PYTHON
import socket
from pythonping import ping
s=socket.socket()
s.bind(('localhost',8000))
s.listen(5)
c,addr=s.accept()
while True:
    hostname=c.recv(1024).decode()
    try:
        c.send(str(ping(hostname, verbose=False)).encode())
    except KeyError:
        c.send("Not Found".encode())
~~~
### SERVER:
~~~PYTHON
import socket
s=socket.socket()
s.connect(('localhost',8000))
while True:
 ip=input("Enter the website you want to ping:")
 s.send(ip.encode())
 print(s.recv(1024).decode())
~~~
## Output
### CLIENT
![image](https://github.com/SGokul2005/4.Execution_of_NetworkCommends/assets/147121825/dede3cc2-9bed-4af4-8a98-b5c453c8c824)

### SERVER
![image](https://github.com/SGokul2005/4.Execution_of_NetworkCommends/assets/147121825/e59459b0-a7c0-4288-b25c-ac92936a9a07)
## TRACEROUTE COMMAND
## AIM:
To write the python program for simulating ping command.
## ALGORITHM:
1. Start the program.
2. Get the frame size from the user.
3. To create the frame based on the user request.
4. To send frames to server from the client side.
5. If your frames reach the server, it will send ACK signal to client
otherwise it will sendNACK signal to client.
6. Stop the program

## PROGRAM
~~~PYTHON
from scapy.all import*
target = ["www.google.com"]
result, unans = traceroute(target,maxttl=32)
print(result,unans)
~~~
## OUTPUT
![image](https://github.com/SGokul2005/4.Execution_of_NetworkCommends/assets/147121825/4ec71c51-04c8-4937-a280-cd1a693c7f2f)

## Result
Thus Execution of Network commands Performed 
