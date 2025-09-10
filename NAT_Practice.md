NOTE: public network is always Outside and private network is always inside

Static 
ip nat inside source static (pc IP adress give a public ip) eg (192.168.1.2 200.200.200.1)

Set Inner nat and outer nat 
Eg 
int gi0/1 
ip nat outside
ex
int gi0/0
ip nat inside
exit

Dynamic
ip nat pool (name of the pool) and give the public id range
Eg
ip nat pool DYN_POOL 200.200.200.1 200.200.200.5  netmask 255.255.255.0
access-list 1 permit (192.168.1 0.0.0.255)
ip nat inside source list 1  pool (poolname)
int gi0/1 (public side)
ip nat outside
ex
int gi0/0(private side)
ip nat inside
ex
Alternate or OVERLOAD METHOD
ip nat inside source list 1 interface (the connection to inside ) [eg gi0/1] overload