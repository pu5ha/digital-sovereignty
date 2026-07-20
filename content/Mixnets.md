## What are they?

A mixnet (short for **mix network**) is a privacy network designed to hide **communication metadata**.

Instead of simply hiding a user's IP address, a mixnet makes it much more difficult for an observer to determine **who is communicating with whom**.

It does this by mixing traffic from many users together before forwarding it.

## Why do they exist?

Encryption protects the **contents** of a message.

However, it does not necessarily protect metadata such as:

- Who sent the message
- Who received it
- When it was sent
- How often two parties communicate
- Packet timing
- Packet size

Even if an attacker cannot read the message itself, they may still be able to infer relationships through **traffic analysis**.

Mixnets were designed to make this much harder.

## How they work

Suppose a mix node receives packets from many different users.

Instead of immediately forwarding each packet, it:

1. Collects packets from many users.
2. Waits a short, random amount of time.
3. Randomizes their order.
4. Adds dummy (cover) traffic.
5. Forwards the mixed traffic.

```text
Incoming

Alice
Bob
Charlie
David

↓

Mix Node

↓

Bob
Fake
Alice
David
Fake
Charlie
```

Because packets have been delayed, reordered, and mixed with fake traffic, it becomes much harder to determine which outgoing packet corresponds to which incoming packet.

## Mixnets vs Onion Routing

Both [[Mixnets]] and [[Onion Routing]] route traffic through multiple independent nodes using layered encryption.

The key difference is what each node does.

### Onion Routing (Tor)

Each node immediately forwards packets after decrypting one layer.

```text
Packet

↓

Node

↓

Immediately forwarded
```

This provides low latency, making Tor well suited for web browsing.

### Mixnets (Nym, HOPR)

Each node intentionally delays and mixes packets before forwarding them.

```text
Packets

↓

Mix

↓

Delay

↓

Reorder

↓

Add fake packets

↓

Forward
```

This provides stronger protection against traffic analysis but increases latency.

## Tradeoffs

### Advantages

- Better metadata privacy
- Stronger resistance to traffic analysis
- Harder to correlate senders and receivers
- Better protection against global network observers

### Disadvantages

- Higher latency
- Lower throughput
- Less suitable for interactive applications like web browsing or gaming

## Projects using Mixnets

- [[Nym]]
- [[HOPR]]