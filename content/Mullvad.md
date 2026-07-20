## What is it?

Mullvad is a privacy-focused VPN service founded in 2009 that encrypts your internet traffic and routes it through Mullvad's servers, hiding your IP address from websites, your ISP, and many network observers.

Unlike most VPN providers, Mullvad is designed to collect as little information about its users as possible. It is widely regarded as one of the most privacy-respecting commercial VPNs available.

## Who maintains it?

[[Mullvad VPN AB]], a privately held company based in Gothenburg, Sweden.

## Cost to use?

€5 per month.

Every customer pays the same price regardless of subscription length. Mullvad intentionally avoids long-term contracts and discounts.

## Is it a public good?

No.

Mullvad is a commercial [[VPN]] company. However, it has built a strong reputation within the privacy community by prioritizing user privacy over marketing and growth. It also contributes to open-source software and supports privacy initiatives, including work with the Tor Project.

## How it works

Normally:

```text
You
   ↓
ISP
   ↓
Website
```

Your ISP can see every website you visit, and each website can see your IP address.

With Mullvad:

```text
You
   ↓
Encrypted Tunnel
   ↓
Mullvad VPN Server
   ↓
Website
```

Your ISP can only see that you're connected to Mullvad.

The website sees the IP address of the Mullvad server instead of your own.

Unlike Tor or Nym, Mullvad is a centralized VPN. You are trusting Mullvad to route your traffic and honor its no-logging policy.

## Privacy Features

| Feature | Support | Notes |
|----------|---------|-------|
| Decentralized | ❌ | Operated by a single company |
| Anonymous signup | ✅ | No email or personal information required |
| Anonymous account IDs | ✅ | Login uses a randomly generated account number |
| Unlinkable payments | ✅ | Cash by mail provides strong anonymity |
| Cryptocurrency accepted | ✅ | Supports Bitcoin, Monero, and other payment methods |
| Cash accepted | ✅ | Physical cash can be mailed to Mullvad |
| Metadata protection | ❌ | Hides your IP but not timing or traffic patterns like a mixnet |
| No-logs architecture | ✅ | Designed to avoid storing activity logs |
| RAM-only servers | ✅ | Servers run without persistent storage |
| Open source apps | ✅ | Desktop and mobile applications are open source |
| Open source server | ❌ | VPN server infrastructure is proprietary |
| Independent security audits | ✅ | Regular third-party audits of apps and infrastructure |
| WireGuard support | ✅ | Native support; default protocol |
| OpenVPN support | ✅ | Also supported |
| Kill switch | ✅ | Built into all major clients |
| Multihop | ✅ | Optional bridge/multihop functionality available |
| Obfuscation | ✅ | Supports obfuscation for bypassing censorship |
| DNS leak protection | ✅ | Built in |
| IPv6 leak protection | ✅ | Built in |
| Jurisdiction | Sweden | Subject to Swedish law |

## What makes it different?

Mullvad is built around minimizing the amount of information users must provide.

Some of its distinguishing features include:

- No email address required
- Randomly generated account numbers instead of usernames
- Anonymous cash payments by mail
- Cryptocurrency payments
- Flat €5 monthly pricing
- Open-source applications
- Frequent independent security audits
- Strong transparency around its privacy practices and infrastructure 

## Main limitations

- You must trust Mullvad to operate its servers honestly.
- Mullvad hides your IP address but does not protect against sophisticated traffic analysis in the way that Tor or Nym can.
- Being based in Sweden means it operates within a 14 Eyes country, although its privacy-focused architecture is designed to minimize the information it can provide if compelled.