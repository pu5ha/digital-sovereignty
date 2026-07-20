## What is it?

Proton VPN is a privacy-focused VPN service developed by the team behind Proton Mail. It encrypts your Internet traffic and routes it through Proton's VPN servers, hiding your IP address from websites, your ISP, and other network observers.

Unlike many commercial VPNs, Proton VPN is built around Proton's broader mission of providing privacy-first online services, including email, cloud storage, password management, and calendar.

## Who maintains it?

Proton VPN is developed and operated by [[Proton AG]], a Swiss company headquartered in Geneva.

The company was founded in 2014 by scientists who met at CERN.

## Cost to use?

Proton VPN offers:

- **Free plan** with unlimited bandwidth and servers in a limited number of countries.
- **VPN Plus** paid plan with access to all servers and premium features.

## Is it a public good?

No.

Proton VPN is a commercial service operated by Proton AG.

However, Proton has built a strong reputation for supporting privacy, open-source software, transparency, and digital rights. The company regularly publishes transparency reports, undergoes independent security audits, and contributes to the broader privacy ecosystem.

## How it works

Like other VPNs, Proton VPN creates an encrypted connection between your device and one of Proton's VPN servers.

When you connect:

1. Your device establishes an encrypted connection using either WireGuard or OpenVPN.
2. All of your Internet traffic is securely sent to the Proton VPN server.
3. The VPN server decrypts the traffic and forwards it to its final destination.
4. Websites see the VPN server's IP address instead of your own.

```text
You
   ↓
Encrypted Connection
   ↓
Proton VPN Server
   ↓
Website
```

Your ISP can see that you're connected to Proton VPN but cannot see which websites you're visiting.

## Privacy Features

| Feature | Support | Notes |
|----------|---------|-------|
| Decentralized | ❌ | Operated by Proton AG |
| Anonymous signup | ⚠️ | Can create an account with minimal information, but an account is required |
| Anonymous account IDs | ❌ | Uses Proton accounts rather than random account numbers |
| Unlinkable payments | ⚠️ | Possible with cryptocurrency if used carefully |
| Cryptocurrency accepted | ✅ | Accepts Bitcoin and other cryptocurrencies (availability may vary) |
| Cash accepted | ✅ | Accepts cash payments by mail |
| Metadata protection | ❌ | Hides your IP but does not resist traffic analysis like a mixnet |
| No-logs architecture | ✅ | Independently audited no-logs policy |
| RAM-only servers | ✅ | Uses diskless ("Secure Core" and NetShield infrastructure includes RAM-only servers where applicable) |
| Open source apps | ✅ | Desktop and mobile clients are open source |
| Open source server | ❌ | Server infrastructure is proprietary |
| Independent security audits | ✅ | Apps and no-logs policy have been independently audited |
| WireGuard support | ✅ | Supported |
| OpenVPN support | ✅ | Supported |
| Kill switch | ✅ | Available |
| Multihop | ✅ | Secure Core routes traffic through multiple Proton-owned servers |
| Obfuscation | ✅ | Stealth protocol helps bypass censorship |
| Port forwarding | ✅ | Available on supported platforms |
| DNS leak protection | ✅ | Built in |
| IPv6 leak protection | ✅ | Built in |
| Jurisdiction | Switzerland | Strong privacy laws outside EU and 14 Eyes |

## What makes it different?

Proton VPN distinguishes itself by being part of a broader privacy ecosystem.

Notable features include:

- Free unlimited VPN plan
- Secure Core multi-hop routing through Proton-owned servers
- Stealth protocol for bypassing censorship
- Integration with the Proton ecosystem
- Open-source applications
- Independent security audits
- Swiss jurisdiction
- Strong emphasis on transparency

## Main limitations

- Requires creating a Proton account, making it less anonymous than services like Mullvad.
- You must trust Proton to operate its VPN infrastructure honestly.
- While Secure Core improves protection against compromised exit servers, Proton VPN remains a centralized VPN provider.