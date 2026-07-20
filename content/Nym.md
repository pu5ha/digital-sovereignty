## What it is

Nym is an open-source privacy network that uses a **mixnet** to protect communication metadata.

Like [[Tor]], Nym hides a user's IP address. However, Nym is designed to solve an additional problem: **traffic analysis**.

For example, imagine an attacker can observe both:

- Packets entering the privacy network
- Packets leaving the privacy network

With [[Tor]], they may be able to correlate an incoming packet with an outgoing packet simply by matching their timing and size.

Nym makes this much more difficult by mixing traffic from many users together, introducing small delays, changing packet order, and adding dummy traffic. This makes it much harder to determine which sender is communicating with which receiver.

Its primary products are the Nym Mixnet, [[NymVPN]], SDKs, and network infrastructure for privacy-preserving applications.

## Who maintains it?

The software is primarily developed by [[Nym Technologies]], a company founded in 2018.

The network itself is operated by independent node operators around the world.

## Cost to use?

Running applications on the mixnet requires paying node operators.

The network uses the NYM token to compensate operators for forwarding traffic and providing privacy.

Unlike [[Tor]], Nym is **not free infrastructure** in the long run—it is designed to economically incentivize people to provide bandwidth.

## Is it a public good?

Partially.

Nym is:

- Open source
- Permissionless
- Decentralized
- Privacy-focused

However, unlike [[Tor]], development is led by a private company and the network is sustained through crypto-economic incentives rather than donations and grants.

## Main limitation

Nym provides stronger metadata privacy than [[Tor]], but at the cost of higher latency.

This makes it less suitable for normal web browsing and better suited for applications like messaging, transaction broadcasting, private RPC, and other communication where a small delay is acceptable.

## How Nym works

Nym uses a **mixnet** instead of onion routing.

Like Tor, traffic passes through multiple nodes.

However, instead of immediately forwarding packets, each node:

- Collects packets from many users
- Adds dummy (cover) traffic
- Randomizes packet ordering
- Waits briefly before forwarding

This process makes it much harder for an observer to correlate incoming and outgoing traffic.

The tradeoff is increased latency.

## Tor vs Nym

| Tor | Nym |
|------|-----|
| Onion routing | Mixnet |
| Low latency | Higher latency |
| Optimized for browsing | Optimized for metadata privacy |
| Volunteer-operated | Token-incentivized node operators |
| Hides IP well | Better protection against traffic analysis |
