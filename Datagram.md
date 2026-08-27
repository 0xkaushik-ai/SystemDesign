A datagram is an independent unit of data sent across a network.

  Each datagram contains enough information to be routed separately, such as source and destination
  addresses.

  The most common example is a UDP datagram:

  UDP datagram
   ├── UDP header
   └── Application data

  UDP datagrams are:

  - Fast and lightweight
  - Independent of one another
  - Not guaranteed to arrive
  - Not guaranteed to arrive in order
  - Not automatically retransmitted

  Example uses:

  - DNS queries
  - Video calls
  - Online gaming
  - Live streaming
  - Some market-data systems

  ### Datagram vs TCP

  TCP: reliable, ordered stream of bytes
  UDP: independent datagrams with lower overhead

  A datagram is similar to sending separate postcards: each one can take a different route, arrive
  late, arrive out of order, or never arrive.
 
 
