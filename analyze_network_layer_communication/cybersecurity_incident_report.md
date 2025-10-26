# Cybersecurity Incident Report

| Section 1: Identify the type of attack that may have caused this network interruption                                     |     |
| :------------------------------------------------------------------------------------------------------------------------ | --- |
| One potential explanation for the website's connection timeout error message is: The logs show that: This event could be: |     |
|                                                                                                                           |     |

The type of attack is a SYN flood attack where an attacker will send high volumes SYN packets to the server. The server is degraded and ultimately fail as it is overloaded with requests.

| Section 2: Explain how the attack is causing the website to malfunction                                                                                                                                                                                                                                                                          |
| :----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| When website visitors try to establish a connection with the web server, a three-way handshake occurs using the TCP protocol. Explain the three steps of the handshake: 1\. 2\. 3\. Explain what happens when a malicious actor sends a large number of SYN packets all at once: Explain what the logs indicate and how that affects the server: |

1. The initial SYN (synchronize) packet is sent to the server by the sender
2. The server then responds with a SYN, ACK (synchronize acknowledge) packet back to the sender
3. After receiving he SYN, ACK then sender sends back a ACK packet which establishes the connection between the sender and server

When a malicious actor sends a large number of SYN packets, the server is flooded with the requests and it begins to degrade in performace until it eventually cannot respond anymore and the server times out.

In the log, we are using WireShark (a packet sniffer) to check the logs of the network. You can see that on line 47-51 was a legimate user which complets the TCP handshake and the protocol switched to HTTP.
The initial attack started on line 52 and it completes the TCP handshake but the attacker continues to send SYN packets in high volume.
The server begins to degrade as more and more SYN packets from the attacker is sent until the server can no longer keep up and errors out with the time out error.
