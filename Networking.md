# High Performance Browser Networking
### 1. TLS Session Resumption
Issue: The extra latency and computational costs of the full TLS handshake impose serious performence penalty on application.

Solution:
The first Session Identifiers (RFC 5246) resumption mechanism was introduced in SSL 2.0, which allowed the server to create and send a 32-byte session identifier as part of its ServerHello message during the full TLS negotiation we saw earlier
Specifically, the client can include the session ID in the ClientHello message to indicate to the server that it still remembers the negotiated cipher suite and keys from previous handshake and is able to reuse them
Leveraging session identifiers allows us to remove a full roundtrip, as well as the overhead of public key cryptography, which is used to negotiate the shared secret key.
### Using Shared TLS Cache
### Session Tickets
In practice, deploying session tickets across a set of load-balanced servers also requires some careful thinking and systems architecture: all servers must be initialized with the same session key, and an additional mechanism is required to periodically and securely rotate the shared key across all servers.
