## What is it?

WireGuard is a modern VPN protocol that creates an encrypted tunnel between your device and a VPN server. It is designed to be faster, simpler, and easier to audit than older VPN protocols like OpenVPN and IPsec.

Unlike Mullvad or Proton VPN, WireGuard is **not** a VPN service. It is the technology that many VPN providers use to securely transport your Internet traffic.

## Who maintains it?

WireGuard was created by **Jason A. Donenfeld**, a security researcher and Linux kernel developer.

Today it is an open-source project maintained by Donenfeld and contributors from the Linux and networking communities. It is also built directly into the Linux kernel.

## Cost to use?

Free and open source.

Anyone can use, inspect, or build software using WireGuard.

## Is it a public good?

Yes.

WireGuard is an open-source protocol that has become one of the standard building blocks for secure networking. It is used by commercial VPN providers, businesses, and individuals around the world.

## How it works

The purpose of WireGuard is to create a secure, encrypted connection between your device and a VPN server.

Without WireGuard (or another VPN protocol), your computer has no standard way to securely send all of its Internet traffic to a VPN server.

When you connect, WireGuard:

1. Verifies that you're talking to the correct VPN server using public-key cryptography.
2. Establishes shared encryption keys between your device and the VPN server.
3. Creates an encrypted connection (often called an *encrypted tunnel*).
4. Encrypts every packet sent through that connection.
5. The VPN server decrypts the packets and forwards them to their final destination.

```text
You
   ↓
Encrypted WireGuard Connection
   ↓
VPN Server
   ↓
Website
```

Unlike HTTPS, which secures individual application connections (such as your browser connecting to a website), WireGuard secures your entire network connection. Once the encrypted connection is established, all applications on your device—your browser, email client, messaging apps, and more—can send their traffic securely through the VPN.
## Privacy Features

| Feature | Support | Notes |
|----------|---------|-------|
| Open source | ✅ | Fully open source |
| Modern cryptography | ✅ | Uses a small set of well-studied cryptographic algorithms |
| Minimal codebase | ✅ | Around 4,000 lines of kernel code, making it easier to audit than older VPN protocols |
| High performance | ✅ | Designed for low latency and high throughput |
| Built into Linux kernel | ✅ | Included since Linux 5.6 |
| Cross-platform | ✅ | Available on Linux, macOS, Windows, iOS, Android, and BSD |
| Metadata protection | ❌ | Encrypts traffic but does not hide timing or traffic patterns |
| Anonymous by itself | ❌ | Requires a VPN provider or your own server |
| Decentralized | ❌ | Peer-to-peer protocol, not a decentralized network |
| Traffic obfuscation | ❌ | WireGuard packets are identifiable unless additional obfuscation is used |

## What makes it different?

Compared to older VPN protocols, WireGuard emphasizes simplicity.

Some of its advantages include:

- Much smaller codebase than OpenVPN or IPsec
- Easier to audit for security issues
- Faster connection setup
- Better roaming support when switching between Wi-Fi and cellular networks
- Excellent performance on mobile devices
- Uses a fixed suite of modern cryptographic algorithms instead of supporting many legacy options

## Main limitations

- WireGuard is only a transport protocol—it does not provide a VPN service on its own.
- It does not provide anonymity or metadata protection beyond encrypting the connection.
- It does not hide traffic patterns like mixnets such as Nym or HOPR.
- Some VPN providers must build additional systems around WireGuard to manage user identities and dynamic IP addresses while preserving privacy.