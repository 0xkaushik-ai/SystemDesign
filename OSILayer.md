# OSI layer 
- Its the seven layered archtiecture .

  7. Application
  6. Presentation
  5. Session
  4. Transport
  3. Network
  2. Data Link
  1. Physical

   Layer              Responsibility                               Examples                          
  ━━━━━━━━━━━━━━━━━  ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━  ━━━━━━━━━━━━━━━━━━━━━━━━━━━
   7. Application     Services used by applications                HTTP, DNS, SMTP
  ─────────────────  ───────────────────────────────────────────  ───────────────────────────
   6. Presentation    Data format, encryption, compression         TLS, JSON, JPEG
  ─────────────────  ───────────────────────────────────────────  ───────────────────────────
   5. Session         Starts and manages communication sessions    Session control
  ─────────────────  ───────────────────────────────────────────  ───────────────────────────
   4. Transport       End-to-end delivery, reliability, ports      TCP, UDP
  ─────────────────  ───────────────────────────────────────────  ───────────────────────────
   3. Network         Routing between networks                     IP, routers
  ─────────────────  ───────────────────────────────────────────  ───────────────────────────
   2. Data Link       Local delivery using MAC addresses           Ethernet, Wi-Fi, switches
  ─────────────────  ───────────────────────────────────────────  ───────────────────────────
   1. Physical        Sends raw bits through hardware              Cables, radio, fiber

  Example when opening a website:

  HTTP request
    ↓
  TCP segment
    ↓
  IP packet
    ↓
  Ethernet frame
    ↓
  Electrical/radio signals

  At the sender, data moves down the layers. At the receiver, it moves back up.

  In real-world development, the TCP/IP model is used more often, but OSI is very useful for
  interviews and troubleshooting. For system design, focus especially on:

  - Application: HTTP and APIs
  - Transport: TCP, UDP, WebSockets
  - Network: IP and routing
  - Data Link: Ethernet, frames, and MAC addresses
  - Physical: bandwidth and network hardware


1. Physical layer
     Sends raw bits as electrical, radio, or light signals through cables, Wi-Fi, or fiber.

  2. Data Link layer
     Delivers data between devices on the same local network using MAC addresses. It creates frames
     and detects local transmission errors.
     Examples: Ethernet, Wi-Fi.

  3. Network layer
     Moves data between different networks using IP addresses. It determines routing.
     Example: IP and routers.

  4. Transport layer
     Provides communication between applications. It uses ports and may provide reliability,
     ordering, retransmission, and flow control.
     Examples: TCP, UDP.

  5. Session layer
     Establishes, manages, and terminates communication sessions between applications. In modern
     systems, this responsibility is often handled by application protocols or libraries.

  6. Presentation layer
     Converts data into usable formats and may handle encryption or compression.
     Examples: JSON encoding, serialization, TLS, compression.

  7. Application layer
     Provides network services directly to applications, such as web requests, name lookup, and
     email.
     Examples: HTTP, DNS, SMTP.

