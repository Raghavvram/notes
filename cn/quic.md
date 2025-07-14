# QUIC (Quick UDP Internet Connections)

**Last Updated:** 2025-07-15

QUIC (Quick UDP Internet Connections) is a modern transport layer network protocol designed by Google. It aims to reduce latency and improve the performance of web applications by addressing some of the limitations of TCP. QUIC is the underlying protocol for HTTP/3.

## Key Features

*   **Reduced Latency:** QUIC significantly reduces connection and transport latency. It features a 0-RTT (Zero Round-Trip Time) connection establishment for returning clients, meaning data can be sent immediately without waiting for a handshake to complete.
*   **Multiplexing without Head-of-Line Blocking:** Unlike TCP, where a single lost packet can block all subsequent packets, QUIC allows for multiple independent streams over a single connection. If one stream is blocked, others can continue, eliminating head-of-line blocking.
*   **Integrated Security:** QUIC has built-in TLS 1.3, ensuring that all connections are encrypted by default. This tight integration of security and transport reduces the overhead of a separate TLS handshake.
*   **Connection Migration:** QUIC allows for seamless connection migration. If a client's IP address changes (e.g., switching from Wi-Fi to cellular), the connection can continue without interruption. This is a significant improvement over TCP, where a change in IP address would terminate the connection.
*   **Improved Congestion Control:** QUIC uses a more advanced and pluggable congestion control algorithm than traditional TCP. This allows for better performance over a variety of network conditions.

## QUIC Handshake

The QUIC handshake is designed to be fast and secure. It combines the transport and cryptographic handshake into a single process.

1.  **Initial Handshake (1-RTT):** For a new connection, the client sends a `ClientHello` message to the server. The server responds with a `ServerHello`, its certificate, and other necessary information. This process takes one round trip.
2.  **Zero RTT (0-RTT):** For a returning client, the client can send encrypted data immediately along with the `ClientHello`. This is possible because the client and server have previously established a shared secret.

## QUIC and UDP

QUIC is built on top of UDP (User Datagram Protocol), a connectionless and unreliable protocol. QUIC adds the reliability and connection-oriented features that UDP lacks:

*   **Reliability:** QUIC implements its own reliability mechanisms, including packet retransmission, to ensure that data is delivered correctly.
*   **Flow Control:** QUIC has its own flow control mechanisms to prevent a sender from overwhelming a receiver.
*   **Ordered Delivery:** While QUIC allows for out-of-order delivery of packets for different streams, it ensures that data within a single stream is delivered in the correct order.

## HTTP/3 and QUIC

HTTP/3, the latest version of the Hypertext Transfer Protocol, uses QUIC as its transport protocol. This is a major departure from previous versions of HTTP, which used TCP.

By using QUIC, HTTP/3 benefits from all of QUIC's features, including reduced latency, multiplexing, and improved security. This results in a faster and more reliable web experience.