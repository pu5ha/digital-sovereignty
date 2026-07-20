## What is it?

The InterPlanetary File System (IPFS) is an open-source, peer-to-peer protocol for storing and sharing files.

Instead of locating files by **where** they are stored (such as a server or URL), IPFS locates files by **what** they are. Every file is identified by a unique cryptographic hash called a **Content Identifier (CID)**.

This approach, known as **content addressing**, makes files easier to verify, distribute, and retrieve from multiple peers.

## Who maintains it?

IPFS was originally created by [[Protocol Labs]] in 2015.

Today, IPFS is maintained as an open-source project by contributors from around the world. While Protocol Labs continues to play a major role in its development, the protocol is open, and anyone can build software, run nodes, or contribute to the ecosystem.

## Cost to use?

The IPFS protocol is free to use.

Running an IPFS node only requires your own computing resources, such as storage space, bandwidth, and electricity.

## Is it a public good?

Yes.

IPFS is open source, permissionless, and designed as public Internet infrastructure rather than a commercial cloud storage service.

Anyone can run a node, contribute to the network, or build applications on top of the protocol.

## How it works

When you add a file to IPFS:

1. The file is split into one or more blocks.
    
2. Each block is cryptographically hashed.
    
3. These hashes are combined into a unique **Content Identifier (CID)**.
    
4. Your node announces that it can provide the file.
    
5. Other peers can retrieve the file using its CID.

Unlike traditional web hosting, files can be downloaded from **any peer** storing the content rather than a single server.

```text
Traditional Web

You
   ↓
https://example.com/file.pdf
   ↓
Single Server
```

```text
IPFS

You
   ↓
Content Identifier (CID)
   ↓
Peer A
Peer B
Peer C
```

As long as at least one peer continues hosting the content, it remains available.

## Key concepts

### Content addressing

Traditional websites identify files by their location.

```text
https://example.com/image.png
```

IPFS identifies files by their contents.

```text
bafybeigdyrzt...
```

If the contents change, the CID also changes.

### Content Identifier (CID)

A CID is a cryptographic fingerprint of a file.

Because it is derived from the file itself:

- Identical files always produce the same CID.
    
- Modified files always produce a different CID.
    
- Users can verify they received the correct file without trusting the source.

### Peer-to-peer network

IPFS nodes communicate directly with one another.

Any node storing a file can provide it to others, improving redundancy and reducing reliance on centralized servers.

### Pinning

Files remain available only while at least one node stores them.

**Pinning** tells an IPFS node to keep a file permanently instead of allowing it to be removed during garbage collection.

Many applications use pinning services to ensure important files remain online.

## What makes it different?

Unlike traditional cloud storage, IPFS:

- Uses content addressing instead of location addressing.
    
- Allows files to be served by many peers.
    
- Verifies files automatically using cryptographic hashes.
    
- Eliminates single points of failure.
    
- Is permissionless and open source.
    
- Works well as infrastructure for decentralized applications.

## Main limitations

- Files are not guaranteed to remain available unless someone continues hosting or pinning them.
    
- Retrieving content can be slower than using a nearby centralized server.
    
- IPFS is a distribution protocol, not a permanent storage network.
    
- Discovering peers may take time for less frequently accessed content.
    
- Public content is visible to anyone who knows its CID.

## Common use cases

- Hosting decentralized websites
    
- NFT metadata and media
    
- Decentralized applications (dApps)
    
- Software distribution
    
- Academic and archival content
    
- Sharing large files
    
- Content-addressed backups