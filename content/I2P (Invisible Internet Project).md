## What it is

I2P (Invisible Internet Project) is a free, open-source anonymous overlay network that allows users to communicate and host services without revealing their network identity.

Unlike [[Tor]], which is primarily designed for anonymously accessing the public Internet, I2P is primarily designed for anonymous communication **within the I2P network itself**.

Its main services include anonymous websites ("eepsites"), messaging, file sharing, and peer-to-peer applications.

https://www.youtube.com/watch?v=KhG29riqVUE
## Who maintains it?

I2P is an open-source community project.

There is no nonprofit equivalent to [[The Tor Project, Inc.]] that centrally coordinates development. Instead, the software is maintained by volunteer developers and contributors from around the world.

## Cost to use?

Free.

There are no subscriptions, tokens, or fees required to use the I2P network.

## Is it a public good?

Yes.

I2P is:

- Open source
- Free to use
- Permissionless
- Community maintained
- Volunteer operated
- Designed for privacy and censorship resistance rather than profit

## Main limitation

I2P is significantly smaller than Tor, resulting in fewer users and services.

It is also designed primarily for communication within the I2P ecosystem, making it less convenient for anonymously browsing the regular Internet.

## How I2P works

Like [[Tor]], I2P routes traffic through multiple peers to hide who is communicating.

However, instead of using a single three-hop circuit, I2P builds **two separate tunnels** for every connection:

```text
Outbound Tunnel
You
 ↓
Peer
 ↓
Peer
 ↓
Destination

Inbound Tunnel
Destination
 ↓
Peer
 ↓
Peer
 ↓
You
```

Every participant contributes bandwidth by routing traffic for others.

Traffic flows through independent inbound and outbound tunnels that are rebuilt periodically, making long-term tracking more difficult.

Unlike Tor, there are no dedicated Guard, Middle, or Exit relays. Every participant can act as a router for the network.

## Tor vs I2P

| Tor | I2P |
|------|-----|
| Anonymous access to the public Internet | Anonymous communication within the I2P network |
| Three-hop circuits | Separate inbound and outbound tunnels |
| Dedicated exit relays | Primarily no exit relays |
| Coordinated by [[The Tor Project, Inc.]] | Community-developed |
| Larger user base | Smaller but more internally focused |
