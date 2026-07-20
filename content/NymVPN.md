## What is it?

NymVPN is a privacy-focused VPN built on top of the [[Nym]] network.

Unlike traditional VPNs, NymVPN gives users two privacy modes:

- **Fast Mode** – A decentralized, 2-hop VPN based on AmneziaWG (a censorship-resistant version of WireGuard) designed for everyday browsing, streaming, and downloading.
- **Anonymous Mode** – A 5-hop [[Mixnets|mixnet]] that provides much stronger metadata privacy by mixing traffic, adding cover traffic, and introducing delays. It is designed for activities like messaging, crypto transactions, and private communication rather than high-speed browsing.

## Who maintains it?

NymVPN is developed by [[Nym Technologies]].

The underlying network is operated by independent node operators around the world.

## Cost to use?

NymVPN is a paid subscription service.

Unlike [[Tor]], which is free, NymVPN charges users to fund the operation of its decentralized network and compensate node operators. Users can pay with traditional payment methods or cryptocurrencies, and the system also supports privacy-preserving payments using [[zk-nyms]]. 

## How it works

NymVPN gives users a choice between two routing models.

### Fast Mode

```text
You
   ↓
Entry Node
   ↓
Exit Node
   ↓
Internet
```

- 2-hop decentralized VPN
- Based on AmneziaWG (WireGuard)
- Faster, lower latency
- Suitable for browsing, streaming, and downloads

### Anonymous Mode

```text
You
   ↓
Gateway
   ↓
Mix Node
   ↓
Mix Node
   ↓
Mix Node
   ↓
Gateway
   ↓
Internet
```

- 5-hop decentralized mixnet
- Uses layered encryption and packet mixing
- Adds cover traffic and timing delays
- Much stronger protection against traffic analysis
- Higher latency

## Why it's different from a traditional VPN

Traditional VPNs ask you to trust a single company.

```text
You
   ↓
VPN Company
   ↓
Internet
```

That company can potentially associate your IP address with your online activity.

NymVPN distributes trust across independently operated nodes so that no single operator can link your identity to your activity by design. Anonymous Mode goes further by using a mixnet to resist traffic analysis. 

## Main limitations

- Anonymous Mode is significantly slower than a traditional VPN.
- Fast Mode provides stronger privacy than a conventional VPN but does not offer the same metadata protection as the mixnet.
- Better suited for privacy-sensitive activities than high-performance gaming or streaming.

## Node Operation

Anyone can become a Nym node operator by running the open-source node software and bonding the required amount of [[NYM Token]].

The basic lifecycle looks like this:

1. Install the Nym node software.
2. Bond (stake) NYM tokens to register the node.
3. Keep the node online with good uptime and performance.
4. The node is periodically selected to participate in the active network.
5. When selected, the node forwards encrypted traffic through the [[Mixnets]].
6. The node earns NYM rewards based on factors such as stake, performance, and uptime.

Users who don't want to run a node can also delegate their NYM to an existing operator. Delegators share in the rewards while helping well-performing nodes attract more stake.

Unlike [[Tor]], where relay operators volunteer bandwidth, Nym economically incentivizes node operators through token rewards. The goal is to create a sustainable, permissionless privacy network where anyone can contribute bandwidth and earn compensation.