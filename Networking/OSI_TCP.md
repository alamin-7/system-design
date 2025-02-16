# OSI 7 layers

7. Application - User interaction, data formatting, and application services. (HTTP, FTP, SMTP). 

6. Presentation - Data formatting, encryption, and compression. 

5. Session - Establishing, managing, and terminating connections. 

4. Transport - Ensuring reliable data transfer. (TCP, UDP). The data is split into small packets.
   Each packet is given a sequence   number and a checksum. The receiving end reassembles the packets in.

3. Network - Routing and forwarding data between devices. (IP, ICMP). Routers determine the best path to destination server. 

2. Data Link - Error-free transfer of data frames between two devices on the same network. (Ethernet, Wi-Fi)

1. Physical - Transmission of raw bits over a physical medium (copper, fiber, wireless).



# How 7 layers matter to Backend Developent

. Troubleshooting API requests (Application Layer)

. Ensuring secure HTTPS connections (Presentation Layer) 

. Handling long-lived WebSocket connections (Session Layer)

. Optimizing API performance using TCP or UDP (Transport Layer) 

. Understanding how cloud load balancing and routing works (Network Layer)

. Debugging networking issues using tools like Wireshark, netstat, curl (All Layers) 


# TCP

What is TCP: Transmission Control Protocol. Ensures reliable data transfer between devices. It is a 
connection-oriented protocol. It establishes a connection before sending data. It ensures that data is
delivered in the correct order. It also ensures that data is delivered without errors.

# How TCP HandShake happen

TCP Handshake: 3-way handshake. It is a process of establishing a connection between two devices. 
It involves three steps: SYN, SYN-ACK, ACK. Details are as follows: 