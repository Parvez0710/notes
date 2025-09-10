It's the mapping of private IP address to public IP address and vice versa

Private IP range
A 10.0.0.0-10.255.255.255
B 172.16.0.0-172.31.255.255
C 192.168.0.0- 192.168.255.255

Types 
Static NAT
1 private --- 1 public ip (one - one connection)

Dynamic NAT
Multiple private ip ----- pool of public IP( multiple private IP- a pool of public IP generally 3-5 Public IP)
Disadvantage of the public IP's are busy the msges are to been in waiting

Overloading NAT or PAT(Port Address Translation)
Multiple private ip address into one public ip address 
I changed the port of the lone public address