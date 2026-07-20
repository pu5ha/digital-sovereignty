## What is it?

Session is a privacy-focused messaging application designed to minimize both message content exposure and metadata collection.

Like Signal, Session provides end-to-end encrypted messaging. Unlike Signal, it does not require a phone number and routes messages through a decentralized network to make it more difficult to determine who is communicating with whom.

Session is built on the **Session Network**, a decentralized network of community-operated nodes, and is designed for users who prioritize anonymity alongside secure messaging.

## Who maintains it?

Session is developed by the [[Session Technology Foundation]], a nonprofit organization dedicated to developing open-source, privacy-preserving communication technologies.

The Session Network itself is maintained by decentralized node operators rather than a single company.

## Cost to use?

Session is free to download and use.

There are no advertisements or subscription fees.

## Is it a public good?

Largely, yes.

Session is open source, developed by a nonprofit foundation, and built on decentralized infrastructure operated by independent node operators.

## How it works

Every conversation on Session is protected with end-to-end encryption.

When you send a message:

1. Your device encrypts the message.
    
2. The message is routed through multiple Session Network nodes.
    
3. Each node only knows the previous and next hop in the route.
    
4. The recipient decrypts the message using their private keys.
    

```text
You
   ↓
Encrypted Message
   ↓
Session Node
   ↓
Session Node
   ↓
Session Node
   ↓
Recipient
```

Unlike traditional messaging services, Session does not rely on centralized servers or phone numbers for user accounts.

Each user is identified by a cryptographic public key known as a **Session ID**.

## Privacy Features

| Feature                     | Support | Notes                                                                                                     |
| --------------------------- | ------- | --------------------------------------------------------------------------------------------------------- |
| Decentralized               | ✅       | Messages are routed through the Session Network                                                           |
| Open source client          | ✅       | Android, iOS, Desktop, and source code are publicly available                                             |
| Open source server          | ✅       | Session Network software is open source                                                                   |
| End-to-end encryption       | ✅       | Enabled by default                                                                                        |
| Forward secrecy             | ⚠️      | Protects past messages if keys are later compromised, though not as extensively as Signal                 |
| Post-compromise security    | ❌       | Does not automatically recover security after key compromise like Signal                                  |
| Metadata protection         | ✅       | Onion routing and decentralized infrastructure reduce metadata exposure                                   |
| Onion routing               | ✅       | Messages are routed through multiple nodes                                                                |
| No phone number required    | ✅       | Accounts are created using cryptographic Session IDs instead of phone numbers                             |
| Usernames                   | ⚠️      | Uses Session IDs by default; optional human-readable names are available through the Session Name Service |
| Multi-device support        | ⚠️      | Supported but less seamless than Signal                                                                   |
| Independent security audits | ⚠️      | Components have been reviewed, though not to the same extent as the Signal Protocol                       |
| Cost                        | Free    | Community supported                                                                                       |

## What makes it different?

Session prioritizes anonymity as much as message encryption.

Its distinguishing characteristics include:

- No phone number required
    
- Decentralized messaging network
    
- Onion-routed message delivery
    
- Strong metadata protection
    
- Accounts identified by cryptographic Session IDs
    
- Open-source software
    
- Nonprofit development
    
- No advertisements
    
- No centralized message servers
    

## Main limitations

- Larger message delays due to decentralized routing.
    
- Weaker forward secrecy and post-compromise security than Signal.
    
- Smaller user base than mainstream messaging applications.
    
- Session IDs are less user-friendly than phone numbers or usernames.
    
- Decentralized routing can consume more bandwidth and increase latency.