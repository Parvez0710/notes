Tags:[[Desktop_Environment]]
Centralised naming server which provides usernames to users 
Package to install
dnf install freeipa-server freeipa-server-dns freeipa-client -y 

vim /etc/hosts
Go in
(my ip address) server.(Server.net) server
ipa-server-install --setup-dns
(Give the name)
(Give the domain)
(Create a realm name) MOSTLY ITS DOMAIN NAME AND PASS
THEN ADMIN PASS
(YES) ITS SHOWS IP 
(YES)
IF NEED NO CHANGE IP THEN ENTER OR YES


NETBIOS NAME
FORWARD POLICY REVERSE POLICY AND CERTIFICATE CREATED

kinit admin (TO INITIATE KERBAROS)
PASS
klist ( LIST KERBAROS)
firewall-cmd --add-service={freeipa-ldap,freeipa-ldaps,dns,ntp} --permanefirewall-cmd --reload


setenforce 0
IN ICOGNATO IN THE WEB ADDRESS domain name/ipa/ui/

TOO ADD USERS IN TERMINAL
ipa user-add username --first=<firstname> --last=<lastname>--password
ipa user-find username TO SEARCH FOR USERS

##Client Config
dnf install freeipa-client -y //INSTALLATION 
nmcli connection modify ens33/32 ipv4.dns  //SERVER IP ADDRESS 
nmcli connection down ens33/32; nmcli connection up ens 32
ipa-client-install --server=class.codiculture.local --domain codicature.local
authselect enable-feature with-mkhomedir
systemctl enable --now oddjobd

Reclipa server
//IN SERVER  ipa hostgroup-add-member ipaservers --hosts client.//CLIENT
//IN SERVER  firewall-cmd --add-service=freeipa-replication --permanent

//IN CLIENT NODE firewall-cmd --add-service={freeipa-ldap,freeipa-ldaps,dns,ntp,freeipa-ldaps,dns,ntp,freeipa-replication} --permanent


//IN REPLICA SERVER
dnf install freeipa-server freeipa-server -dns -y
ipa-replica-install --setup-ca --setup-dns --noforwarders
kinit admin
ipa user-find

Replica and environment video ref dic server pt 3 and 4





kill-9 process id