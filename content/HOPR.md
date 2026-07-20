## What is it?

HOPR is an open-source, decentralized privacy network that uses an incentivized [[Mixnets|mixnet]] to hide communication metadata.

Like [[Nym]], HOPR protects not only the content of communication but also metadata such as IP addresses, timing, and communication patterns.

Its primary goal is to provide transport-layer privacy for Web3 applications so that wallets, dapps, AI agents, and other decentralized services do not leak metadata every time they communicate.

## Who maintains it?

HOPR is developed by the [[HOPR Association]], a Swiss nonprofit.

The software is open source, while the network itself is operated by independent node operators around the world.

## Cost to use?

Applications pay to send data through the network.

Node operators stake and earn [[HOPR Token|HOPR]] tokens for relaying traffic and providing cover traffic.

## Is it a public good?

Mostly.

HOPR is:

- Open source
- Permissionless
- Decentralized
- Community governed

Unlike [[Tor]], HOPR relies on crypto-economic incentives rather than volunteers to sustain the network.

## Main limitation

Like other [[Mixnets]], HOPR introduces additional latency.

It is designed for privacy-sensitive communication rather than high-speed web browsing or gaming.

## How HOPR works

Applications send encrypted data into the HOPR mixnet.

Rather than immediately forwarding packets, relay nodes:

- Mix traffic from many users
- Add cover traffic
- Introduce random delays
- Forward packets through multiple relay nodes

This makes it significantly harder for an observer to determine who is communicating with whom.

Unlike traditional VPNs, no single relay knows both the sender and receiver.

## Proof of Relay

One of HOPR's main innovations is **Proof of Relay**.

Instead of trusting that a node forwarded traffic, HOPR uses cryptographic proofs to verify that relay work was actually performed.

Only nodes that successfully relay traffic can claim rewards.

This prevents operators from pretending to relay packets simply to collect rewards.

## HOPR vs Nym

| HOPR | Nym |
|------|------|
| Mixnet | Mixnet |
| Proof of Relay | Different reward mechanism |
| Focus on Web3 transport privacy | Broader privacy infrastructure |
| HOPR token | NYM token |
| Swiss nonprofit | Swiss company (Nym Technologies) + decentralized network |
