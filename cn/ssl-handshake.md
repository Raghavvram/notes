# SSL/TLS Handshake

**Last Updated:** 2025-07-15

The SSL/TLS handshake is a protocol used to establish a secure communication channel between a client and a server. It is the foundation of HTTPS and is responsible for encrypting the communication between your web browser and the websites you visit.

## The Handshake Process

The SSL/TLS handshake involves a series of steps that allow the client and server to authenticate each other, agree on an encryption algorithm, and exchange keys.

1.  **ClientHello:** The client initiates the handshake by sending a `ClientHello` message to the server. This message contains:
    *   The TLS versions the client supports.
    *   A list of cipher suites the client supports.
    *   A random string of bytes known as the "client random."

2.  **ServerHello:** The server responds with a `ServerHello` message. This message contains:
    *   The TLS version that will be used for the connection.
    *   The cipher suite that will be used.
    *   The server's SSL certificate.
    *   A random string of bytes known as the "server random."

3.  **Authentication:** The client verifies the server's SSL certificate with the certificate authority (CA) that issued it. This ensures that the client is communicating with the correct server and not a malicious third party.

4.  **Key Exchange:** The client generates a "premaster secret" and encrypts it with the server's public key (which is extracted from the SSL certificate). The encrypted premaster secret is then sent to the server.

5.  **Session Key Generation:** Both the client and the server use the client random, the server random, and the premaster secret to generate the same session keys. These session keys are symmetric, meaning the same key is used for both encryption and decryption.

6.  **Finished Messages:** The client and server exchange `Finished` messages, which are encrypted with the session key. This confirms that the handshake is complete and that the client and server are ready to exchange encrypted data.

## Importance of the Handshake

The SSL/TLS handshake is a critical part of web security. It ensures that:

*   **Confidentiality:** The data exchanged between the client and server is encrypted and cannot be read by third parties.
*   **Integrity:** The data is not tampered with during transmission.
*   **Authentication:** The client can be sure that it is communicating with the correct server.