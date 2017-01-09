# notmail
A secure replacement for email based on blockchain and distributed graph technologies.

# Overview

Unlike standard email, **notmail** does not actually "send" email messages.  Instead, encrypted message content is securely stored in a user-selected, web-addressable storage location identified by a URI, while the metadata specifying the sender, recipients, URI, and decryption key are stored in a public, cryptographically secure block graph (distributed database).

The "block graph" could be a "block chain"; however, a more generalized distributed data stucture than a linear block chain may be a more suitable data structure for this application, given the balance of security and scalability requirements.  The **notmail** server nodes will form a peer-to-peer network that collectively validate and publish the graph across the network.

A **notmail** client may be paired with a **notmail** server to create a "full node".  Server nodes should also implement a client-proxy, to service requests from remote clients through a JSON API.  Communication between the remote client and the client-proxy will be over HTTPS.

For compatibility with standard email clients, the **notmail** server will also support SMPT and IMAP client interfaces.

**notmail** users (message senders and receivers) will have secure, verifiable, digital identities featuring a public key.  The public key may be used to identify message senders and receivers in the message metadata.

The server, the client-proxy, the standard client, and the client-facing interfaces will be implemented in the Go programming language.
