# gRPC

gRPC is an RPC framework commonly used for backend-to-backend communication. It uses Protocol Buffers and normally runs over HTTP/2.

```text
Service A ── gRPC ──> Service B
```

Standard gRPC is not directly browser-native. Browser applications can use gRPC-Web through a compatible proxy, such as Envoy.

Use gRPC when strongly typed contracts, efficient binary serialization, and streaming are valuable. Consider REST for public APIs and broad browser compatibility.
