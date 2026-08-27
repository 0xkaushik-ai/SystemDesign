# Packet and Frame 
- A packet and a frame are containers used to move data across a network but they belong to different layers .
A packet is mainly an IP-layer unit. It contains:

  - Source IP address
  - Destination IP address
  - Transport data, such as TCP or UDP data

  Example:

  Device A: 192.168.1.10
  Device B: 142.250.190.14

  Routers read packet IP addresses to decide where to forward the data.

### Frame

  A frame is a data-link-layer unit used for delivery on one local network segment. It contains:

  - Source MAC address
  - Destination MAC address
  - An IP packet inside it

  Switches read MAC addresses to deliver frames within a local network.

  ### Simple analogy

  Imagine sending a parcel:

  - Application data = the item
  - Packet = the addressed parcel for the overall destination
  - Frame = the local delivery truck packaging used for the next hop

  At each router, the old frame is removed and a new frame is created for the next network. The IP
  packet generally continues toward the destination.

  For system design, the key difference is:

  > Packets use IP addresses for network-to-network delivery; frames use MAC addresses for local-    
  > network delivery.                                                                                
 

Multicasting means sending one message to a specific group of receivers.

  Sender
    ↓
  Network
    ├── Receiver A
    ├── Receiver B
    └── Receiver C

  The sender transmits the message once, and the network forwards it only to devices that joined the
  multicast group.

  ### Comparison

  - Unicast: one sender → one receiver
  - Broadcast: one sender → every device on the network
  - Multicast: one sender → selected group of receivers

  Example: A trading platform publishes market-price updates to a multicast group. Only subscribed
  trading servers receive them.

  In IPv4, multicast addresses commonly range from:

  224.0.0.0 to 239.255.255.255

  Devices join and leave multicast groups using protocols such as IGMP.

  Multicast is efficient for live video, IPTV, service discovery, and financial market data. However,
  public browsers generally do not directly receive IP multicast, so websites usually use a backend
  fan-out service and WebSockets instead.
 
