## What is it?

Lokinet is a decentralized, low-latency anonymous overlay network that onion-routes **all IP traffic**, not just web browsing.

Unlike [[Tor]], which primarily routes TCP traffic through a browser or SOCKS proxy, Lokinet operates at the **network layer (Layer 3)**. This means it can anonymize almost any IP-based application, including web browsing, messaging, voice calls, games, and other software without requiring application-specific support. 

## Who maintains it?

Lokinet is developed by the [[Open Privacy Technology Foundation (OPTF)]], the nonprofit behind [[Session]].

The network itself is operated by independent service node operators who stake tokens to participate. 

## Cost to use?

Using Lokinet is free.

The underlying network is funded by economically incentivized service nodes rather than volunteers. Operators stake tokens and receive rewards for running reliable infrastructure. 

## Is it a public good?

Mostly.

Lokinet is:

- Open source
- Permissionless
- Decentralized
- Privacy-focused

Unlike [[Tor]], relay operators are economically incentivized rather than purely volunteer-run.

## Main limitation

Lokinet has a much smaller network and user base than [[Tor]].

Its anonymity set is therefore smaller, although proponents argue that economically incentivized nodes provide more reliable infrastructure and better resistance to Sybil attacks. 

## How Lokinet works

Like [[Tor]], Lokinet uses onion routing through multiple independent nodes.

The major difference is where it operates.

Tor works at the **application layer**, so applications generally need to explicitly use Tor (for example through Tor Browser or a SOCKS proxy).

Lokinet works at the **network layer**, creating an anonymous virtual IP network.

Applications simply send normal IP packets.

```text
Application
      ↓
Operating System
      ↓
Lokinet
      ↓
Service Nodes
      ↓
Internet
```

Because Lokinet routes IP packets instead of only TCP streams, it can support a much wider range of applications without modification.

## Tor vs Lokinet

| Tor | Lokinet |
|------|----------|
| Application-layer onion router | Network-layer onion router |
| Primarily TCP traffic | Any IP-based traffic |
| Best for anonymous browsing | Best for general-purpose anonymous networking |
| Volunteer relay operators | Token-incentivized service nodes |
| Large anonymity set | Smaller but economically incentivized network |
