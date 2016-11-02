# notmail
A secure replacement for email based on blockchain related technologies.

# Overview

Unlike standard email, **notmail** does not actually "send" email messages.  Instead, encrypted messages are securely stored in a single, user-determined, web-addressable storage location specified by a URI, while the metadata specifying the originator, the recipients, the URI, and a decryption key are stored in a public, cryptographically secured block graph that is distributed across participating server nodes.

The "block graph" could be a "block chain"; however, a more generalized distributed data stucture than a linear block chain may be a more suitable data structure for this application, given the balance of security and scalability requirements.  The ##notmail## server nodes will form a peer-to-peer network that collectively validate and publish the graph block across the network.

A **notmail** client may be paired with a **notmail** server to create a "full node".  Server nodes should also implement a client-proxy, to service requests from remote clients through a JSON API.  Communication between the remote client and the client-proxy will be over HTTPS.

For compatibility with standard email clients, the ##notmail## server will also support SMPT and IMAP client interfaces.

**notmail** users (message senders and receivers) will have secure, verifiable, digital identities featuring a public key.  The public key may be used to identify the sender and receivers of messages in the message metadata.

The server, the client-proxy, the standard client, and the client-facing interfaces will be implemented in the Go programming language.


