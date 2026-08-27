# Multicasting

Multicasting sends one message to a selected group of receivers.

- Unicast: one sender to one receiver
- Broadcast: one sender to every device on a network
- Multicast: one sender to subscribed receivers

IPv4 multicast addresses range from `224.0.0.0` to `239.255.255.255`. Devices join groups using protocols such as IGMP.

Multicast is useful for market data, IPTV, and live media in controlled networks. Browsers generally use backend fan-out plus WebSockets instead of receiving IP multicast directly.
