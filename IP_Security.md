Site to Site Connectivity

Uses Of VPN
HQ------>Branch office encrypted path way

Advantages

DATA Confidentiality
  Encryption 
DATA Integrity
 Preventing from tampering
Authentication 
 Pre-Shared key
 PKI -public key Infrastructure 
 Digital Certification -SSL/TLS


Access Control

Voice and video
 VoIP - Voice Over IP
 E- Commerce transactions
 IOT

Types
 Remote Access VPN
 Client-to-site VPN -endpoint VPN
Site to Site VPN
 Intranet VPN --->LAN
 MPLS VPN
 SSL/TLS VPN


IP Security Phases

1. Initiation
       a. Initiator
       b. Responder
2. Proposal exchange 
       a. Encryption algorithm, Integrity       algorithm , Diffie-Hellman Key exchange type protocols
3. IKE Phase 1- Internet Key Exchange
       a. Authentication and key exchange
           Authentication methods
           Methods
           First tunnel will be created
           Security Association 
4. IKE Phase 2- ISAKMP
       a. Negotiate and agree
       b. Second Tunnel will be created
       c. Data transmitted 
5. Termination 
        a. End of connection



Different types of mode 

1. Transparent Mode
        Client to client
        Eg whatsapp
        IP Header is not encrypted 

2. Tunnel Mode
        Gateway to gateway 
         IP Header is encrypted 
         Eg VPN




Difference in packet 

Normal packet
Consists of
    IP Header--TCP Header--DATA

Transport mode packet
IP header--AH Heade--TCP header--DATA
where 
AH is Authentication Header which later becomes 
ESP is Encapsulating Security Payload

Tunnel packet 
New IP header--AH Header--IP Header--TCP header--DATA




Tunnel Settings 

Authentication Methods 
Kerberos
X.509 - SSL/TLS - Digital Signature 
Pre-shared key

Ip filtering 
Source traffic
Destination traffic
Protocol
Sourceport, destport
IP filler action
Permit,Block,negotiate

Encryption 
ESP- integration and encryption 
AH- integrity only
Custom



Internet Key Exchange 
IKEv1
1998
IKEv2
2005

--> Terms
SA- Security Association 
        Establishment of shared security attributes between two network entities
        Attributes
        Cryptographic algorithm,mode,traffic, encryption key,parameters
VID- Vendor IDS
         Used to determine peer support for features like NAT, Dead peer, detection fragmentation 
Nonce
         A randomly generated number sent by the initiator used to check even after username password matches
KE- Key Exchange 
       Deffie -Hellman DH secure key exchange process
Idi/Idr
Identify Initiator / Identity Responder
Packet 
Main mode packet exchange 
Aggressive Mode packet exchange


Main mode 
It's has 6 Phases before converting messages it encrypted version







Aggressive mode
It does the same work has main mode in 3 phases


ISAKMP ( Internet Security Association and Key Management protocol)
Is does SA by it self

