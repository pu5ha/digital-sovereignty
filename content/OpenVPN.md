## What is it?

OpenVPN is an open-source VPN protocol that creates a secure, encrypted connection between your device and a VPN server. It has been one of the most widely used VPN protocols since its release in 2001 and is supported by nearly every commercial VPN provider.

Unlike Mullvad or Proton VPN, OpenVPN is **not** a VPN service. It is the technology many VPN providers use to securely transport your Internet traffic.

## Who maintains it?

OpenVPN was created by **James Yonan**.

Today, the open-source project is maintained by the OpenVPN community and OpenVPN Inc., the company behind the protocol.

## Cost to use?

Free and open source.

Anyone can use, inspect, or build software using OpenVPN.

## Is it a public good?

Yes.

OpenVPN is open-source software that has become one of the foundational technologies for secure networking. It is used by VPN providers, businesses, governments, and individuals around the world.

## How it works

Like WireGuard, the purpose of OpenVPN is to create a secure, encrypted connection between your device and a VPN server.

When you connect, OpenVPN:

1. Verifies the identity of the VPN server using TLS certificates.
2. Performs a TLS handshake to establish shared encryption keys.
3. Creates an encrypted connection between your device and the VPN server.
4. Encrypts every packet sent through that connection.
5. The VPN server decrypts the packets and forwards them to their final destination.

```text
You
   ↓
Encrypted OpenVPN Connection
   ↓
VPN Server
   ↓
Website
```

Once the encrypted connection is established, all applications on your device can securely send their traffic through the VPN.
## Privacy Features

| Feature | Support | Notes |
|----------|---------|-------|
| Open source | ✅ | Fully open source |
| Modern encryption | ✅ | Uses TLS with strong encryption algorithms |
| Cross-platform | ✅ | Available on all major operating systems |
| Metadata protection | ❌ | Encrypts traffic but does not hide traffic patterns |
| Anonymous by itself | ❌ | Requires a VPN provider or your own server |
| Decentralized | ❌ | Client-server protocol |
| Traffic obfuscation | ✅ | Can run over TCP or UDP and can be configured to resemble HTTPS traffic, helping bypass some censorship |
| Mature ecosystem | ✅ | Widely supported by VPN providers and networking equipment |

## What makes it different?

OpenVPN prioritizes compatibility and flexibility.

Some of its strengths include:

- Extremely mature and battle-tested
- Highly configurable
- Can use either UDP (faster) or TCP (more reliable)
- Uses the same TLS technology trusted by web browsers
- Supported by nearly every VPN provider and enterprise firewall

Because it builds on TLS, OpenVPN integrates well with existing security infrastructure and certificate management systems.

## Main limitations

- Larger and more complex than WireGuard.
- Slower connection establishment because of the TLS handshake.
- Larger codebase, making it more difficult to audit than WireGuard.
- Generally lower performance and higher CPU usage than WireGuard.