## What is it?

A Virtual Private Network (VPN) encrypts your internet traffic and routes it through a remote server before it reaches the Internet. This hides your IP address from the websites and services you use while preventing your Internet Service Provider (ISP) from seeing the contents of your traffic.

VPNs are one of the most common tools for improving online privacy, securing public Wi-Fi connections, bypassing geographic restrictions, and reducing network surveillance.

## How it works

Without a VPN:

```text
You
   ↓
ISP
   ↓
Website
```

Your ISP can see the websites you visit, and each website can see your IP address.

With a VPN:

```text
You
   ↓
Encrypted Tunnel
   ↓
VPN Server
   ↓
Website
```

Your ISP can only see that you're connected to a VPN server.

The website sees the VPN server's IP address instead of yours.

## What VPNs protect

VPNs can hide:

- Your IP address
- Your approximate location
- Your browsing activity from your ISP
- Your traffic from others on the same Wi-Fi network
- DNS requests (if the VPN provides its own DNS)

## What VPNs do NOT protect

A VPN does **not** automatically provide anonymity.

Depending on the VPN provider, it may still be possible to learn:

- When you connected
- How much data you transferred
- Traffic timing patterns
- Which VPN server you used

The VPN provider itself can potentially observe your traffic unless it is encrypted end-to-end (HTTPS).

VPNs also do not prevent:

- Browser fingerprinting
- Tracking cookies
- Account-based tracking (e.g. logging into Google)
- Malware
- Phishing attacks

## VPN vs Tor

| VPN | Tor |
|------|-----|
| Single trusted provider | Volunteer relay network |
| Fast | Slower |
| Excellent for everyday browsing | Better for anonymity |
| Hides your IP | Hides your IP |
| Provider can potentially observe traffic | Trust distributed across multiple relays |
| Limited resistance to traffic analysis | Better resistance to network surveillance |

## VPN vs Mixnets

| VPN | Mixnet (e.g. Nym, HOPR) |
|------|-------------------------|
| Hides IP address | Hides IP address |
| Does not hide traffic timing | Adds delays and mixes traffic |
| Minimal latency | Higher latency |
| Good for everyday browsing | Designed for strong metadata privacy |
| Trusts one provider | Trust distributed across many nodes |

## Common VPN Protocols

Modern VPNs typically use one or more tunneling protocols:

- [[WireGuard]]
- [[OpenVPN]]

These protocols define how encrypted tunnels are established between your device and the VPN server.

## Choosing a VPN

Important privacy considerations include:

- Logging policy
- Anonymous signup
- Anonymous payment options
- Open-source applications
- Independent security audits
- Jurisdiction
- Modern protocols (WireGuard/OpenVPN)
- Kill switch
- DNS leak protection
- IPv6 leak protection
- RAM-only servers

## Main limitations

A VPN shifts trust rather than eliminating it.

Instead of trusting your ISP with your network traffic, you trust the VPN provider.

For users seeking stronger anonymity or protection against sophisticated traffic analysis, tools like [[Tor]], [[Nym]], or [[HOPR]] provide additional privacy at the cost of performance.