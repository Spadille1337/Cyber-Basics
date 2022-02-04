## Naming, Addressing & Forwarding
A network `address` is any logical or physical address that uniquely distinguishes a network node or device over a computer or telecommunications network. It is a numeric/symbolic number or address that is assigned to any device that seeks access to or is part of a network.
After you receive your assigned network IP address and you have given the IP addresses to your systems, the next task is to assign `names` to the hosts. Then you must determine how to handle name services on your network. You use these names initially when you set up your network and later when you expand your network through routers, bridges, or PPP.
When a packet arrives at a router’s input link, the router must move the packet to the appropriate output link. This is known as `forwarding`. For example, a packet arriving from Host H1 to Router R1 must be forwarded to the next router on a path to H2.

## MAC Address
- Media Access Control Address
- Unique adress encoded by manufacturer onto Network Interface Card(NIC)
- Each NIC has globally unique MAC address
- MAC Address are used for Data Link Layer
- MAC address can be considerd as Physical address
- has hexadecimal format (48-bit)

## IP Address
- belogs to Layer 3: Network Layer
- these are logical address mapped to Physical device
- able to route accross the network or over the world even
- logically assigned physical address
- they can change or our comp can have multiple IP address throughout the day
- they are not hard encoded, these are address provided to our computer by network

## Subnet Mask
- Subnet Masks are what that let us know what position is a host portion and what portion is a network portion 
- For eg. if we have our computer IP on rthe network like `192.168.1.1`('192.168.1 -> Network ID, 1 -> Host ID') then in this case, we will have a a lot of networks and only 254 hosts(as we can't use 0 and 255)

## Gateway
- A computer that sits between different networks or applications. 
- The gateway converts information, data or other communications from one protocol or format to another.

## Classification of IP Addresses
In the IPv4 IP address space, there are five classes: A, B, C, D and E:

**Class A**
Class A addresses are for networks with large number of total hosts. Class A allows for 126 networks by using the first octet for the network ID. The first bit in this octet, is always zero. The remaining seven bits in this octet complete the network ID. The 24 bits in the remaining three octets represent the hosts ID and allows for approximately 17 million hosts per network. Class A network number values begin at 1 and end at 127.
-   Public IP Range: 1.0.0.0 to 127.0.0.0
    -   First octet value range from 1 to 127
-   Private IP Range: 10.0.0.0 to 10.255.255.255 
-   Subnet Mask: 255.0.0.0 (8 bits)
-   Number of Networks: 126
-   Number of Hosts per Network: 16,777,214

**Class B**
Class B addresses are for medium to large sized networks. Class B allows for 16,384 networks by using the first two octets for the network ID. The first two bits in the first octet are always 1 0. The remaining six bits, together with the second octet, complete the network ID. The 16 bits in the third and fourth octet represent host ID and allows for approximately 65,000 hosts per network. Class B network number values begin at 128 and end at 191.
-   Public IP Range: 128.0.0.0 to 191.255.0.0
    -   First octet value range from 128 to 191
-   Private IP Range: 172.16.0.0 to 172.31.255.255 
-   Subnet Mask: 255.255.0.0 (16 bits)
-   Number of Networks: 16,382
-   Number of Hosts per Network: 65,534

**Class C**
Class C addresses are used in small local area networks (LANs). Class C allows for approximately 2 million networks by using the first three octets for the network ID. In a class C IP address, the first three bits of the first octet are always 1 1 0. And the remaining 21 bits of first three octets complete the network ID. The last octet (8 bits) represent the host ID and allows for 254 hosts per network. Class C network number values begins at 192 and end at 223.
-   Public IP Range: 192.0.0.0 to 223.255.255.0
    -   First octet value range from 192 to 223
-   Private IP Range: 192.168.0.0 to 192.168.255.255 
-   Special IP Range: 127.0.0.1 to 127.255.255.255 
-   Subnet Mask: 255.255.255.0 (24 bits)
-   Number of Networks: 2,097,150
-   Number of Hosts per Network: 254

**Class D**
Class D IP addresses are not allocated to hosts and are used for multicasting. Multicasting allows a single host to send a single stream of data to thousands of hosts across the Internet at the same time. It is often used for audio and video streaming, such as IP-based cable TV networks. Another example is the delivery of real-time stock market data from one source to many brokerage companies.
-   Range: 224.0.0.0 to 239.255.255.255
    -   First octet value range from 224 to 239
-   Number of Networks: N/A
-   Number of Hosts per Network: Multicasting

**Class E**
Class E IP addresses are not allocated to hosts and are not available for general use. These are reserved for research purposes.
-   Range: 240.0.0.0 to 255.255.255.255
    -   First octet value range from 240 to 255
-   Number of Networks: N/A
-   Number of Hosts per Network: Research/Reserved/Experimental

## Network Address Translation (NAT) 
- It’s a way to map multiple local private addresses to a public one before transferring the information. 
- Organizations that want multiple devices to employ a single IP address use NAT, as do most home routers.

## Domain Name Server (DNS)
A DNS is a directory of domain names that align with IP addresses. They bridge the gap between computer language and human language – keeping both servers and people happy.

## Subnetting
- It is adding additional networks to our standad  public/private ranges
- For eg. `192.168.0.x`
   Now we can have 254 hosts only. For a big organisation, it's not enough wheras for home network it;s more than enough. So we want to break it up into smaller subnets without necessarily going and changing actual IP address. This breaking up of IP into smaller subnets without necessarily going and changing actual IP address is known as subnetting.
   
## Networking Devices 
**Hubs**
- Layer 2 (Data Link Layer) device
- Pass data/information to everyone
- other than sending data, it does nothing like mapping address etc

**Bridges**
- Layer 2 (Data Link Layer) device
- a network device that connects multiple LANs (local area networks) together to form a larger LAN

**Switches**
- Layer 2 (Data Link Layer) device
- Map to MAC address 
- devices on our network which allows us to connect multiple devices that are on the subnet 

**Routers**
- sometimes reffered to as "layer 3 switch"
-  connects different networks together and sends data packets from one network to another
-  can be used both in LANs (Local Area Networks) and WANs (Wide Area Networks)
-  transfers data in the form of IP packets

## Protocols
In networking, a protocol is a set of rules for formatting and processing data. 

Types of Network Protocols are :

**Network Communication Protocols**
These protocols formally describe the formats and rules by which data is transferred over the network.
 
 - **HTTP** : Hyper text transfer protocol (HTTP)  is an application layer protocol that allows the browser and server to communicate.
 - **TCP** : Transmission Control Protocol (TCP) separates data into packets that can be shared over a network.
 - **UDP** : User Datagram Protocol (UDP) works in a similar way to TCP, sending packets of data over the network. The key difference between the two is that TCP ensures a connection is made between the application and server, but UDP does not.
 - **IRC** : Internet Relay Chat (IRC) is a text-based communication protocol. Software clients are used to communicate with servers and send messages to other clients.

**Network Management Protocols**
Network management protocols help define the policies and procedures used to monitor, manage and maintain your computer network, and help communicate these needs across the network to ensure stable communication and optimal performance across the board.

- **SNMP** : Simple Network Management Protocol (SNMP) is used to monitor and manage network devices.
- **ICMP** : Internet Control Message Protocol (ICMP) is primarily used for diagnostic purposes.

**Network Security Protocols**
Network Security Protocols work to ensure that data in transit over the network's connections stays safe and secure. These protocols also define how the network secures data from any attempts to review or extract said data by illegitimate means.

- **SSL** : A Secure Socket Layer (SSL) is a network security protocol primarily used for ensuring secure internet connections and protecting sensitive data.
- **SFTP** : Secure File Transfer Protocol (SFTP), as its name might suggest, is used to securely transfer files across a network. Data is encrypted and the client and server are authenticated.
- **HTTPS** : Secure Hypertext Transfer Protocol is the secure version of HTTP.

## Firewalls
A Firewall is a network security device that monitors and filters incoming and outgoing network traffic based on an organization’s previously established security policies. At its most basic, a firewall is essentially the barrier that sits between a private internal network and the public Internet. A firewall’s main purpose is to allow non-threatening traffic in and to keep dangerous traffic out.

## WAPs
- A wireless access point (WAP) is a hardware device or configured node on a local area network (LAN) that allows wireless capable devices and wired networks to connect through a wireless standard, including Wi-Fi or Bluetooth. 
- WAPs feature radio transmitters and antennae, which facilitate connectivity between devices and the Internet or a network.
- A WAP is also known as a hotspot.

## Application Layer
Application layer is the top most layer in OSI and TCP/IP layered model. This layer exists in both layered Models because of its significance, of interacting with user and user applications. This layer is for applications which are involved in communication system.
The application layer provides several protocols which allow any software to easily send and receive information and present meaningful data to its users.

- **DHCP** : DHCP stands for Dynamic Host Configuration Protocol. It provides IP addresses to hosts. Whenever a host tries to register for an IP address with the DHCP server, DHCP server provides lots of information to the corresponding host. DHCP uses port numbers 67 and 68.
-  **FTP/SFTP** : FTP stands for File Transfer Protocol. This protocol helps to transfer different files from one device to another. FTP promotes sharing of files via remote computer devices with reliable, efficient data transfer. FTP uses port number 20 for data access and port number 21 for data control. 
	SFTP (SSH File Transfer Protocol) is a secure file transfer protocol.
- **HTTP/HTTPS** : Hyper text transfer protocol (HTTP)  is an application layer protocol that allows the browser and server to communicate.
	Secure Hypertext Transfer Protocol is the secure version of HTTP.
- **IMAP** : IMAP stands for Internet Message Access Protocol and it allows us to access your email wherever you are, from any device. When you read an email message using IMAP, you aren't actually downloading or storing it on your computer; instead, you're reading it from the email service.
- **LDAP** : Lightweight directory access protocol (LDAP) is a protocol that makes it possible for applications to query user information rapidly. LDAP is a protocol, so it doesn't specify how directory programs work. Instead, it's a form of language that allows users to find the information they need very quickly.
- **POP** : POP(Post Office Protocol) works by contacting your email service and downloading all of your new messages from it. Once they are downloaded onto your PC or Mac, they are deleted from the email service. This means that after the email is downloaded, it can only be accessed using the **same computer**.
- **SMTP** : SMTP stands for Simple Mail Transfer Protocol. It is used to transfer electronic mail from one user to another user. SMTP is used by end users to send emails with ease. SMTP uses port numbers 25 and 587.
- **SNMP** :  Simple Network Management Protocol (SNMP) is used to monitor and manage network devices.
- **SSH** : SSH or Secure Shell is a network communication protocol that enables two computers to communicate (c.f http or hypertext transfer protocol, which is the protocol used to transfer hypertext such as web pages) and share data.
- **Telnet** : Telnet stands for Telecommunications Network. This protocol is used for managing files over the Internet. It allows the Telnet clients to access the resources of Telnet server. Telnet uses port number 23.
- **SSL/TLS** : SSL is a cryptographic protocol that uses explicit connections to establish secure communication between web server and client.
	TLS is also a cryptographic protocol that provides secure communication between web server and client via implicit connections.
