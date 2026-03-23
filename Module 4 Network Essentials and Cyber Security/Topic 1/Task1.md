## UDP


<B>1. What does it mean that UDP is a connectionless protocol?</B>

When we say UDP (User Datagram Protocol) is connectionless, it means:

There is no setup or handshake before sending data (unlike TCP’s 3-way handshake).
Data is sent immediately as independent packets (called datagrams).
There is no guarantee:
that data arrives
that it arrives in order
or that it arrives only once

👉 Think of it like sending postcards—you just send them without confirming delivery.

<B>2. What is the use of checksums in UDP?</B>

A checksum in UDP is used for error detection.

The sender calculates a checksum based on the data.
The receiver recalculates it upon arrival.
If the values don’t match:
The packet is considered corrupted
It is discarded

⚠️ Important:

UDP does NOT fix errors or retransmit data—it only detects them.

<BR>

<B>3. What are port numbers and how does UDP use them?</B>

Port numbers identify specific applications or services on a device.

Each UDP packet contains:
Source port (sender application)
Destination port (receiver application)
Example:
DNS uses port 53
A game or app might use a custom port

👉 UDP uses port numbers to ensure data is delivered to the correct application, not just the correct device.

<B>4. UDP Datagram Diagram </B>

Here’s a simple representation you can recreate in Paint, Visio, or similar:

+----------------------+----------------------+
|   Source Port (16)   | Destination Port (16)|
+----------------------+----------------------+
|     Length (16)      |    Checksum (16)     |
+---------------------------------------------+
|                                             |
|                 Data (Payload)              |
|                                             |
+---------------------------------------------+

<BR>

<img width="742" height="644" alt="image" src="https://github.com/user-attachments/assets/49a20cc1-83d3-4253-ba43-a80ffa870087" />
