## What is it?

BitTorrent is a peer-to-peer protocol for distributing files across the internet.

Instead of downloading an entire file from one central server, users download different pieces from multiple people who already have some or all of the file.

At the same time, users upload the pieces they have already downloaded to others. This allows demand for a popular file to be shared across the entire group rather than overwhelming one server.

## Who created it?

BitTorrent was created by [[Bram Cohen]] and first released in **2001**.

Cohen later co-founded [[BitTorrent, Inc.]] to develop commercial software around the protocol. The protocol itself is open and has many independent client implementations.

## Cost to use

The BitTorrent protocol is free to use.

Users provide their own:

- Internet connection
    
- Bandwidth
    
- Storage
    
- Computing resources

BitTorrent does not include built-in payments for people who distribute files.

## How it works

Suppose someone wants to distribute a large movie file.

### 1. The file is divided into pieces

```text
Movie file
├── Piece 1
├── Piece 2
├── Piece 3
├── Piece 4
└── Piece 5
```

Each piece receives a cryptographic hash so a downloader can verify that it received the correct data.

### 2. Torrent metadata is created

The distributor creates a small `.torrent` file containing information such as:

- The file names
    
- The file sizes
    
- The size of each piece
    
- The hashes of the pieces
    
- Information used to find other peers

The `.torrent` file does not contain the movie itself. It is more like a map describing the data that must be downloaded.

A **magnet link** can provide the information needed to locate the torrent without first downloading a separate `.torrent` file.

### 3. The first seeder shares the file

The original distributor is called a **seeder** because they possess every piece.

```text
Original seeder

Piece 1 ✅
Piece 2 ✅
Piece 3 ✅
Piece 4 ✅
Piece 5 ✅
```

Other users join the group and begin downloading pieces.

This group of users sharing the same torrent is called a **swarm**.

### 4. Peers download different pieces

BitTorrent tries to spread pieces efficiently across the swarm.

```text
Seeder → Piece 1 → User A
Seeder → Piece 2 → User B
Seeder → Piece 3 → User C
```

Now those users can exchange pieces with one another:

```text
User A gives Piece 1 to User B
User B gives Piece 2 to User C
User C gives Piece 3 to User A
```

The original seeder no longer has to send every piece separately to every user.

### 5. Users upload while downloading

A person who has only part of the file is called a **peer** or sometimes a **leecher**.

```text
User A

Piece 1 ✅
Piece 2 ✅
Piece 3 ❌
Piece 4 ❌
Piece 5 ❌
```

User A can immediately upload Pieces 1 and 2 to other users while still downloading the remaining pieces.

This is what makes BitTorrent scale well:

> Every downloader can also become an uploader.

### 6. The file is reconstructed

Once a user has downloaded and verified every piece, their BitTorrent client puts the pieces back together.

```text
Piece 1
+
Piece 2
+
Piece 3
+
Piece 4
+
Piece 5
      ↓
Complete movie file
```

The user can then remain online as a seeder and continue distributing the file.

## How peers find each other

BitTorrent clients can discover other members of a swarm through several methods.

### Trackers

A tracker is a server that tells peers how to contact one another.

```text
Your client
     ↓
Tracker
     ↓
List of peers sharing the file
```

The tracker normally does not store or transfer the file. It only helps coordinate peer discovery.

### Distributed Hash Table

BitTorrent can also use a **Distributed Hash Table**, or DHT, to discover peers without relying on one tracker.

```text
Torrent identifier
        ↓
Distributed network of BitTorrent clients
        ↓
Peers sharing that torrent
```

### Peer exchange

Once connected, peers can tell one another about additional peers in the swarm.

This reduces dependence on any single discovery method.

## Key concepts

### Torrent

A torrent is the metadata describing the files and their pieces.

It does not normally contain the files themselves.

### Magnet link

A magnet link identifies the torrent using a cryptographic value and lets the client locate its metadata and peers through the network.

### Swarm

A swarm is the group of peers currently sharing a particular torrent.

### Seeder

A seeder has the complete file and continues uploading it.

### Peer

A peer is any participant downloading or uploading pieces.

### Piece

A piece is one portion of the shared file or collection of files.

### Seeding

Seeding means remaining connected after completing the download so others can retrieve pieces from you.

## Availability

BitTorrent does not guarantee that a file will remain available.

A torrent works only while at least one reachable peer still has every required piece.

```text
At least one complete copy remains
              ↓
File can still be downloaded
```

If all complete seeders disappear and the remaining peers collectively lack one piece, nobody can finish the file.

Therefore, BitTorrent is a distribution protocol, not permanent storage.

## Privacy

BitTorrent is not anonymous by default.

Peers commonly expose their IP addresses to:

- Trackers
    
- Other peers
    
- DHT participants

Anyone observing a public swarm may be able to see which IP addresses are sharing a torrent.

BitTorrent also does not encrypt files automatically. Private data should be encrypted before distribution when confidentiality is required.

## BitTorrent and IPFS

BitTorrent and [[IPFS]] both divide files into verifiable pieces and distribute them between peers.

|Feature|BitTorrent|[[IPFS]]|
|---|---|---|
|Primary unit|Torrent or swarm|Content Identifier|
|Main purpose|Efficiently distribute a defined set of files|Address and retrieve content-addressed data|
|File verification|Piece hashes|CIDs and linked blocks|
|Peer discovery|Trackers, DHT and peer exchange|Distributed routing and provider records|
|Permanent storage|No|No|
|Data structure|Fixed torrent file set|General content-addressed graph|
|Updating content|Usually create a new torrent|New data creates a new CID|

A simplified distinction is:

> BitTorrent organizes people around downloading a particular torrent.

> IPFS organizes content around globally reusable identifiers.

## BitTorrent and Filecoin

|Technology|Main purpose|
|---|---|
|BitTorrent|Peers voluntarily distribute files|
|[[Filecoin]]|Providers are paid and required to prove storage|

BitTorrent has no storage contracts, collateral or cryptographic proof that someone will continue storing the file.

## BitTorrent and Arweave

|Technology|Main purpose|
|---|---|
|BitTorrent|Efficient file distribution while seeders remain|
|[[Arweave]]|Long-term storage funded through a one-time payment|

BitTorrent is useful for distributing popular files cheaply, but Arweave is designed to preserve information even after the original uploader leaves.

## Common uses

- Distributing large open-source software releases
    
- Sharing public datasets
    
- Game updates
    
- Media distribution
    
- Archives
    
- Peer-to-peer file sharing
    
- Reducing bandwidth pressure on central servers

BitTorrent itself is content-neutral, although it has also been widely used to share copyrighted material without authorization.

## What makes it different?

BitTorrent becomes more efficient as more users participate.

With a traditional server:

```text
One server
   ↓
Must send the full file to everyone
```

With BitTorrent:

```text
Original source
      ↓
Users exchange pieces with one another
      ↓
Distribution capacity grows with the swarm
```

This makes it especially effective for distributing large, popular files.

## Main limitations

- Files disappear when nobody continues seeding all required pieces.
    
- There is no built-in payment for storage or bandwidth.
    
- Users’ IP addresses are generally visible.
    
- Downloads may be slow when few peers are available.
    
- A swarm can become incomplete if an essential piece disappears.
    
- BitTorrent does not provide permanent storage.
    
- Files are not private or encrypted by default.
    
- Torrent indexes and trackers may introduce centralized dependencies.
    
- It is strongly associated with copyright infringement despite having many legitimate uses.

## Simple mental model

```text
BitTorrent:
“Everyone downloading this file should exchange pieces with everyone else.”

IPFS:
“Find the content matching this cryptographic address.”

Filecoin:
“Pay providers to store the content for a fixed period.”

Arweave:
“Pay once to preserve the content indefinitely.”
```