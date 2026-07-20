## What is metadata?

Metadata is **information about a piece of data or a communication**, rather than the data or communication itself.

It provides context such as who, when, where, and how something occurred without revealing the underlying contents.

For example, if someone sends the message:

> "Meet me at 6:00 PM."

The message itself is the **content**.

Metadata includes information such as:

- Who sent the message
    
- Who received it
    
- When it was sent
    
- The sender's IP address
    
- The recipient's IP address
    
- The size of the message
    
- The communication protocol used
    

A simple way to think about it is:

> **Content is what was said. Metadata is everything surrounding the communication.**

## Why does metadata matter?

Metadata can reveal a surprising amount about a person's life, even if the contents of every message remain encrypted.

For example, metadata can reveal:

- Who communicates with whom
    
- How frequently they communicate
    
- When people are active
    
- Where they are connecting from
    
- Social and organizational relationships
    
- Behavioral patterns over time
    

In many cases, this information is enough to identify individuals, map social networks, or infer sensitive activities without ever reading a single message.

## Metadata vs content

|Content|Metadata|
|---|---|
|The actual information being communicated|Information about the communication|
|The text of an email|Sender and recipient|
|A phone conversation|Call duration|
|A photo|When and where it was taken|
|A website's contents|The website you visited and when|

### Observable metadata

Observable metadata is information that exists while a communication is taking place.

Examples include:

- Source and destination IP addresses
    
- Message timing
    
- Packet sizes
    
- Routing information
    

This information is often necessary for networks to function.

### Stored metadata

Stored metadata is information that is intentionally retained after the communication has ended.

Examples include:

- Connection logs
    
- Historical IP addresses
    
- Communication timestamps
    
- Contact lists
    
- Call records

Many privacy-focused technologies are designed to minimize or eliminate stored metadata, even if some metadata must be temporarily observable to deliver a communication.

## Why can't metadata be completely eliminated?

Most communication systems require at least some metadata to function.

For example:

- A messaging service must know where to deliver a message.
    
- Internet routers need destination addresses to forward packets.
    
- A web server needs to know where to send its response.
    

Because of this, completely eliminating metadata is often impossible.

Instead, privacy technologies try to:

- Minimize how much metadata is exposed.
    
- Avoid storing metadata longer than necessary.
    
- Make communications harder to correlate.
    
- Hide communication patterns from observers.

## How different technologies protect metadata

Different privacy technologies focus on protecting different kinds of metadata.

- **End-to-end encrypted messaging apps** like [[Signal]] protect message contents but still require some observable metadata to deliver messages.
    
- **VPNs** hide your IP address from the websites you visit, but the VPN provider can still observe your connections.
    
- **Tor** makes it difficult to link users to the websites they access by routing traffic through multiple relays.
    
- **Mixnets** like [[Nym]] go a step further by mixing traffic from many users and adding cover traffic, making communication patterns much harder to analyze.
    
- **Decentralized messaging systems** like [[SimpleX Chat]] and [[Briar]] are designed to reduce the amount of metadata that centralized servers can observe or store.

Each technology addresses different parts of the metadata problem, which is why they are often complementary rather than interchangeable.

## Key takeaway

Encryption answers:

> **"What was said?"**

Metadata answers questions like:

- Who communicated?
    
- With whom?
    
- When?
    
- Where?
    
- How often?
    
- For how long?
    

Strong privacy requires protecting both the contents of communications **and** the metadata surrounding them.