## What is it?

Signal is an end-to-end encrypted messaging application that allows people to securely send messages, make voice and video calls, and share files.

Unlike traditional messaging platforms, Signal is designed so that only the sender and intended recipients can read messages. The Signal Foundation cannot access message contents, contacts, or call data.

Today, Signal is widely regarded as the gold standard for private messaging and its encryption protocol is used by numerous other messaging platforms.

## Who maintains it?

Signal is developed by **Signal Messenger LLC**, a subsidiary of the [[Signal Foundation]], a nonprofit organization headquartered in the United States.

## Cost to use?

Signal is free to download and use.

There are no subscriptions, advertisements, or premium features.

## Is it a public good?

Largely, yes.

Signal is operated by a nonprofit foundation whose mission is to make private communication universally accessible. Development is funded primarily through donations and grants rather than advertising or selling user data.

## How it works

Every conversation on Signal is protected with end-to-end encryption.

When you send a message:

1. Your device encrypts the message before it leaves your phone.
    
2. The encrypted message is sent through Signal's servers.
    
3. Signal's servers deliver the encrypted message but cannot read its contents.
    
4. Only the recipient's device has the keys needed to decrypt and read the message.
    

```text
You
   ↓
Encrypted Message
   ↓
Signal Server
   ↓
Encrypted Message
   ↓
Recipient
```

Signal's servers act only as message relays. They do not possess the encryption keys needed to decrypt user conversations.

## Privacy Features

| Feature                     | Support | Notes                                                                                                                                                                |
| --------------------------- | ------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Decentralized               | ❌       | Operated by the Signal Foundation                                                                                                                                    |
| Open source client          | ✅       | Android, iOS, and Desktop apps are open source                                                                                                                       |
| Open source server          | ✅       | Server software is open source                                                                                                                                       |
| End-to-end encryption       | ✅       | Enabled by default for all messages and calls                                                                                                                        |
| Forward secrecy             | ✅       | Compromising future keys does not expose past messages                                                                                                               |
| Post-compromise security    | ✅       | Sessions automatically recover after key compromise                                                                                                                  |
| [[Metadata]] protection     | ⚠️      | Minimizes stored metadata, but some network metadata (such as IP addresses, timing, and routing information) is still observable while messages are being delivered. |
| Sealed Sender               | ✅       | Helps hide the sender's identity from Signal's servers                                                                                                               |
| Disappearing messages       | ✅       | Built in                                                                                                                                                             |
| Group messaging             | ✅       | End-to-end encrypted                                                                                                                                                 |
| Voice & video calls         | ✅       | End-to-end encrypted                                                                                                                                                 |
| Username support            | ✅       | Can communicate without sharing your phone number                                                                                                                    |
| Phone number required       | ⚠️      | Required for account creation, though usernames reduce sharing afterward                                                                                             |
| Multi-device support        | ✅       | Desktop and additional devices supported                                                                                                                             |
| Independent security audits | ✅       | Signal Protocol has undergone extensive review                                                                                                                       |
| Cost                        | Free    | Donation supported                                                                                                                                                   |

## What makes it different?

Signal prioritizes privacy above engagement or monetization.

Some of its distinguishing characteristics include:

- End-to-end encryption enabled by default
    
- Open-source clients and server software
    
- Operated by a nonprofit foundation
    
- Widely trusted Signal Protocol
    
- Minimal metadata collection
    
- No advertisements
    
- No tracking
    
- No algorithmic feeds
    
- No data sold to advertisers
    

## Main limitations

- Uses centralized servers for message delivery.
    
- Phone numbers are still required during registration.
    
- Contacts must also use Signal to benefit from end-to-end encryption.
    
- While Signal minimizes metadata, it cannot eliminate all network metadata because messages are routed through centralized infrastructure.