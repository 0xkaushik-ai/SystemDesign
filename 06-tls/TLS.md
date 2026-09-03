# TLS

- This evolve from the is previous encryption protocol called ssl (Secure socket layer) .
TLS secures communication by providing confidentiality, integrity, and server authentication. HTTPS is HTTP protected by TLS.

```text
Client ── handshake and certificate verification ──> Server
Client ═════ encrypted application data ════════════> Server
```

During the handshake, the parties agree on algorithms, verify the server certificate through trusted Certificate Authorities, and establish a symmetric session key. Symmetric encryption then protects normal traffic efficiently.

TLS protects data in transit; it does not automatically protect data stored in a server or database.
- To resolve these severe vulnerabilities, engineers introduced complex mathematical cryptography into the network stack.
- There are three main components of the What TLS protocol accomplishes are :- 
  - Encryption 
  - Authetication 
  - Integrity 


- The entire proceess is managed by the tls handshae which happens before the any application data is exchanged . 
-  The two parties use the shared symmetric session key to encrypt all subsequent communication. Symmetrical encryption is significantly faster than the public/private key cryptography used during the handshake.


# The standard TLS is not sufficient for securing server to server  communication .Then mTLS solve this . 

- Standard tls is suffiecient for a client-to-server where client is web browser and only need to verisfu the server . 
- However in a zero trust architecte no entity is trusted by default ,regardless of its location (inside or outside the network ) . This is where mTLS become essential . 

- mTLS is security model where both the client and the server authenticate each other . It is built on the same pricnicipal as TLS but with and additional step in the handshake .

- We cant use the mTLS everywhere because is does offers more security but it come with the significant trade-offs. The biggest challenge is certificate lifecycle management .

- In TLs one single server Certiicate can be used for thousands of clients (eg website certificate used by all its user ). In mTLS environment evey client must have its own certificate . For large-scale micorservice  with the hundered of servie this means .
- Issuance: Every service needs a certificate from a trusted internal Certificate Authority (CA).
- Distribution: Certificates must be securely distributed to each service instance. 
- Renewal: Certificates have an expiration date and must be renewed regularly and automatically without causing downtime.
- Revocation: If a service is compromised, its certificate must be immediately revoked to prevent it from communicating with other services.
- Mannualy managing this process is nearly impossible and prone to error . Modern solution like service mesh  are designed to automate this entire process . 

- Choose tls when u are building the public-facing api or website where the clients are wbesite .

- Choose the mTLS when u are securing communication between servie in a distributed system especially with in zero-trust network . And u are building system that require high degree of security and compliance  . 


