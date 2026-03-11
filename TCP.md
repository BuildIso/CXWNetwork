# What is the TCP?
Transmission Control Protocol (TCP) is a fundamental protocol within the Internet Protocol Suite,
primarily responsible for ensuring reliable and ordered delivery of data between applications running on hosts communicating via an IP network.
TCP operates at the transport layer of the OSI model and is connection-oriented, meaning it establishes a connection before data transfer begins and maintains it until the communication is complete.
The TCP header contains several fields that facilitate reliable data transmission:
`0 1 2 3
0 1 2 3 4 5 6 7 8 9 0 1 2 3 4 5 6 7 8 9 0 1 2 3 4 5 6 7 8 9 0 1
+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+
| Source Port | Destination Port |
+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+
| Sequence Number |
+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+
| Acknowledgment Number |
+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+
| Data | |U|A|P|R|S|F| |
| Offset| Reserved |R|C|S|S|Y|I| Window |
| | |G|K|H|T|N|N| |
+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+
| Checksum | Urgent Pointer |
+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+
| Options | Padding |
+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+
| Data |
+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+`
Copier
Source Port: Identifies the sending port.

Destination Port: Identifies the receiving port.

Sequence Number: Used to ensure data is delivered in order.

Acknowledgment Number: Indicates the next expected byte from the sender.

Data Offset: Specifies the size of the TCP header.

Flags: Control bits like URG, ACK, PSH, RST, SYN, and FIN.

Window Size: Indicates the size of the sender's receive window.

Checksum: Used for error-checking the header and data.

Urgent Pointer: Points to urgent data if the URG flag is set.

Options: Additional options for the TCP header.
