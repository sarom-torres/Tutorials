## :incoming_envelope::door: How to obtain network informations in CLI

### Obtain IP, Interface Network and NetMask informations

```
sudo ifconfig
```
### Obtain IP Gateway
```
sudo route -n
```
### Obtain IP DNS 
```
cat /etc/resolv.conf
```
### List all open ports  
```
netstat -lntu
```
Where:
- `-l`: prints only listening sockets
- `-n`: shows port number
- `-t`: enables listing of tcp ports
- `-u`: enables listing of udp ports
