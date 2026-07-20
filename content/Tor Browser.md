Tor Browser is a privacy-focused web browser that routes all web traffic through the [[Tor]] network by default.

It is based on Mozilla Firefox but has been heavily modified by [[The Tor Project, Inc.]] to maximize anonymity and resist tracking.

## Why it exists

Simply routing traffic through the Tor network is not enough to remain anonymous.

Modern browsers leak identifying information through browser fingerprinting, cookies, extensions, and other APIs.

Tor Browser is designed to minimize those leaks so users look as similar as possible.

## How it works

Tor Browser actually consists of two applications:

```text
Tor Browser

├── Tor daemon (Tor client)
└── Modified Firefox browser
```

The Tor daemon builds Tor circuits and handles all communication with the Tor network.

The browser sends all network requests to the Tor daemon through a local SOCKS proxy instead of connecting directly to websites.

```text
Browser
    ↓
Tor daemon
    ↓
Guard Relay
    ↓
Middle Relay
    ↓
Exit Relay
    ↓
Website
```

The browser itself does **not** implement onion routing—it simply uses the Tor client.

## Privacy protections

Beyond routing traffic through Tor, Tor Browser also:

- Blocks or limits browser fingerprinting
- Ships with a standardized browser configuration
- Clears browsing state to reduce tracking
- Disables or restricts many identifying browser APIs
- Discourages installing extensions that make users unique

The goal is to maximize the size of the **anonymity set** by making every Tor Browser user look as similar as possible.

## Cost to use?

Free and open source.

## Who maintains it?

[[The Tor Project, Inc.]]

## Main limitation

Tor Browser only protects traffic that goes through the browser.

Other applications on your computer (Discord, Steam, MetaMask, etc.) do not automatically use Tor unless they are separately configured to do so.