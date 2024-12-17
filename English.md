# Basic-Networking (English)
"A network is like communication between neighbors, which has many emotions. Sometimes harmonious, happy, and peaceful. But it can also be a source of commotion and chaos, with envy and jealousy as the root cause."

+yuumaSSS+

## OSI Model
The OSI (Open Systems Interconnection) model is a theoretical-conceptual network model for communication between devices over a network. There is no practical implementation of the OSI model, but the OSI model is useful for understanding how applications can work through a network.

The OSI model has 7 layers that describe how devices communicate. On the sender's side, data travels from the seventh layer to the first layer. Then, on the receiver's side, data travels from the first layer to the seventh layer.

- Application layer (Layer 7)

  The layer that directly interacts with the user's data. At this layer, the data request is prepared to be sent through the network. This layer contains protocols, headers, and cookies.

- Presentation layer (Layer 6)

  The layer that converts data so that systems with different data formats can still exchange information. This layer handles tasks such as encryption-decryption, compression-decompression, and encoding-decoding.

- Session layer (Layer 5)

  The layer responsible for opening, maintaining, and closing sessions. A session is a temporary and interactive exchange of information between two or more communicating devices. This layer helps implement authentication, authorization, and synchronization to function properly.

- Transport layer (Layer 4)

  The layer that ensures the transmitted data is not corrupt (damaged). If it is, the data will be resent. This layer breaks data into smaller forms called segments. Additionally, this layer records the source port and destination port for each segment. The protocols that operate here are TCP and UDP.

- Network layer (Layer 3)

  The layer that breaks segments into smaller forms called packets. A packet has two parts: the header (packet information) and the body (data). The header contains information such as the IP address, total packet size, whether the packet has been further fragmented, and the count of networks the packet has passed through. An IP address is essentially the address used to uniquely identify a computer's connection to a network—like a house address.

- Data link layer (Layer 2)

  The layer that breaks packets into even smaller forms called frames. Frames contain information such as the source MAC address and destination MAC address. A MAC address is a unique identifier embedded in a network card or network interface control, used as a network address. MAC addresses are like private house data. Common protocols at this layer include Ethernet and WiFi.

- Physical layer (Layer 1)

  The layer involving all hardware devices such as routers, cables, and switches. This layer converts frames into bitstreams (binary 1s and 0s) and then transmits or receives them.

## TCP/IP Model
The TCP/IP (Transmission Control Protocol/Internet Protocol) model is a communication model between devices over a network, which is the current standard for the internet community. This model is considered more practical and has only 5 layers (initially 4 layers, but the link layer was split into the data link layer and physical layer for modern efficiency).

As with the OSI model, the order on the sender's side is from the fifth layer to the first layer. On the receiver's side, it is from the first layer to the fifth layer.

- Application layer (Layer 5)

  This layer combines most of the functions of the Presentation Layer and Session Layer from the OSI model.

- Transport layer (Layer 4)

  Same as explained in the OSI model.

- Network layer (Layer 3)

  Same as explained in the OSI model.

- Data link layer (Layer 2)

  Same as explained in the OSI model.

- Physical layer (Layer 1)

  Same as explained in the OSI model.

To simplify and make it easier to remember, you can visualize it like this:
- Physical layer = Planes/Cars/Motorcycles/Bicycles (the medium for delivering packages) and highways  
- Data link layer = Helps deliver packages from one intersection to the next  
- Network layer = Helps navigate the delivery of packages  
- Transport layer = Ensures the correct address  
- Application layer = The contents of the package

## Application Layer Network Protocols
- HTTP

  HTTP (Hypertext Transfer Protocol) is used to transfer data between devices. Hypertext is a well-organized document system using hyperlinks to connect pages within text documents. HTTP is a stateless protocol (it does not retain the client's information history).

- HTTPS

  Similar to HTTP, but HTTP is not encrypted, so hackers can intercept and read HTTP messages. HTTPS (HTTP Secure) is a combination of HTTP and TLS. TLS (Transport Layer Security) is a protocol used to encrypt HTTP messages. TLS is also called SSL (Secure Sockets Layer).

- SMTP

  SMTP (Simple Mail Transfer Protocol) is used to transfer emails between users. This task is performed through email client software (Mail User Agent) used by the user. The User Agent helps users type, format, and store emails until the internet is available. When an email is sent, the delivery process is handled by the Message Transfer Agent, which is usually included in email client software. The Message Transfer Agent uses SMTP to forward emails to another Message Transfer Agent (server-side).

- DNS

  DNS (Domain Name System) is a naming system that maps domain names to IP addresses. DNS makes it easier for humans to remember domain names instead of IP addresses, which consist of numbers and dots.

- FTP

  FTP (File Transfer Protocol) is an internet protocol used to send files over a network from one computer to another.

- SSH

  SSH (Secure Shell) is a cryptographic network protocol for secure data communication, remote login, command execution, and other network services between two computers.
