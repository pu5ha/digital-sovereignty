## What is it?

Onion routing is a networking technique that anonymizes communication by routing traffic through multiple independent relay nodes.

Each relay only knows:

- Where the packet came from
- Where to send it next

No single relay knows both the sender and the final destination.

The name comes from the fact that messages are wrapped in multiple layers of encryption, like the layers of an onion.

## Why does it exist?

Without onion routing, a normal internet connection looks like:

```text
You
   ↓
ISP
   ↓
Website
```

The ISP knows both:

- Who you are
- Where you're going

The website also learns your IP address.

Onion routing separates this knowledge so that no single participant can link the sender to the destination.

## How it works

Suppose you want to visit:

```text
ethereum.org
```

Your client selects three relays:

```text
You
   ↓
Guard Relay
   ↓
Middle Relay
   ↓
Exit Relay
   ↓
Website
```

Before sending the request, your client encrypts it three times:

1. Encrypt with the Exit relay's public key.
2. Encrypt again with the Middle relay's public key.
3. Encrypt again with the Guard relay's public key.

Each relay removes only its own layer of encryption using its private key before forwarding the packet.

### Guard Relay

Knows:

- Your IP address
- The next relay

Does **not** know:

- Final destination

### Middle Relay

Knows:

- Previous relay
- Next relay

Does **not** know:

- Your IP
- Final destination

### Exit Relay

Knows:

- Final destination

Does **not** know:

- Your IP address

The destination website only sees the Exit relay's IP address.

## Why it works

No single relay ever has enough information to reconstruct the full communication path.

| Relay | Knows your IP | Knows destination |
|--------|:-------------:|:-----------------:|
| Guard | ✅ | ❌ |
| Middle | ❌ | ❌ |
| Exit | ❌ | ✅ |

This separation of knowledge is the core security property of onion routing.

## Advantages

- Hides the user's IP address
- Separates sender from destination
- Provides low-latency anonymous communication
- Works well for interactive applications like web browsing

## Limitations

Because packets are forwarded immediately, an attacker observing both ends of the network may be able to correlate packets using their timing and size.

This is known as [[Traffic Analysis]].

Projects such as [[Nym]] and [[HOPR]] address this by using [[Mixnets]], which deliberately delay and mix traffic before forwarding it.

## Projects using Onion Routing

- [[Tor]]
- [[Lokinet]]
- [[Session]] (Onion Requests)

## Onion Routing vs Mixnets

| Onion Routing | Mixnets |
|---------------|----------|
| Packets forwarded immediately | Packets delayed and mixed |
| Lower latency | Higher latency |
| Better for browsing | Better for metadata privacy |
| More vulnerable to traffic analysis | Stronger resistance to traffic analysis |

## Why it matters to Ethereum

Onion routing could improve privacy for:

- RPC requests
- Transaction broadcasting
- Wallet communication
- Accessing Ethereum frontends
- Node networking

It protects the **network path**, but does not provide onchain privacy.

## Mental model

Imagine mailing a package inside three sealed envelopes.

Each relay opens only the envelope addressed to it, learns where to send the package next, and never sees the original sender and final recipient together.

## Related

- [[Tor]]
- [[Mixnets]]
- [[Traffic Analysis]]
- [[Metadata]]
- [[Guard Relay]]
- [[Exit Relay]]