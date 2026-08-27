# Packets and Frames

An IP packet is used for network-to-network delivery and contains source and destination IP addresses.

A frame is used for delivery across one local link and contains source and destination MAC addresses. It carries a packet as its payload.

```text
Ethernet frame
 └── IP packet
      └── TCP segment
           └── Application data
```

At every router hop, the frame is replaced. The IP packet continues toward its destination.
