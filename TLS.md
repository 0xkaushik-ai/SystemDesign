TLS (Transport Layer Security) is a protocol that secures communication between two parties over a
  network.

  When you use:

  https://example.com

  HTTPS means HTTP protected by TLS.

  TLS provides three main guarantees:

  - Confidentiality: Others cannot read the data.
  - Integrity: Others cannot secretly modify the data.
  - Authentication: You can verify that you are communicating with the real server.

  ### Simplified TLS process

  Client                         Server
    │                              │
    │──── ClientHello ────────────>│
    │<─── ServerHello + certificate │
    │──── verifies certificate ───>│
    │<─── secure session established│
    │                              │
    │════ encrypted application data

  During the handshake:

  1. The client and server agree on supported security algorithms.
  2. The server sends its TLS certificate.
  3. The client verifies the certificate through trusted Certificate Authorities.
  4. Both sides securely create a shared symmetric session key.
  5. HTTP data is encrypted using that session key.

  Public-key cryptography is mainly used during the handshake. Symmetric encryption is then used for
  normal data because it is faster.

  TLS protects data while it travels between client and server, but it does not automatically protect
  data after it reaches the server or while it is stored in a database.


