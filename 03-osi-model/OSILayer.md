# OSI Layers

1. Physical — signals and bits
2. Data Link — local delivery, MAC addresses, frames
3. Network — IP addressing and routing
4. Transport — ports, reliability, ordering, flow control (TCP/UDP)
5. Session — manages communication sessions
6. Presentation — formats, encryption, compression
7. Application — services such as HTTP and DNS

```text
Application data → TCP segment → IP packet → Ethernet frame → signals
```

In real systems, the TCP/IP model is used more often, but OSI helps explain failures and interview concepts.
