# TLS

TLS secures communication by providing confidentiality, integrity, and server authentication. HTTPS is HTTP protected by TLS.

```text
Client ── handshake and certificate verification ──> Server
Client ═════ encrypted application data ════════════> Server
```

During the handshake, the parties agree on algorithms, verify the server certificate through trusted Certificate Authorities, and establish a symmetric session key. Symmetric encryption then protects normal traffic efficiently.

TLS protects data in transit; it does not automatically protect data stored in a server or database.
