## What is it?

SimpleX Chat is an open-source messaging application designed to maximize privacy by eliminating permanent user identifiers.

Unlike most messaging platforms, SimpleX does not require:

- Phone numbers
    
- Email addresses
    
- Usernames
    
- Account creation

Instead, each conversation uses unique, one-time cryptographic identifiers. This makes it significantly more difficult to link conversations together or build a social graph.

SimpleX aims to provide end-to-end encrypted messaging while minimizing both message content exposure and metadata collection.

## Who maintains it?

SimpleX Chat is developed by the **[[SimpleX Foundation]]**, a nonprofit organization dedicated to advancing privacy-preserving communication.

The software is open source and developed by contributors from around the world.

## Cost to use?

SimpleX Chat is free to download and use.

There are no advertisements, subscriptions, or premium features.

## Is it a public good?

Largely, yes.

SimpleX is open source, developed by a nonprofit foundation, and focuses on creating privacy-preserving communication infrastructure rather than monetizing users.

## How it works

Every conversation on SimpleX is protected with end-to-end encryption.

Unlike traditional messaging apps, SimpleX does not assign users permanent identities.

Instead, when starting a conversation:

1. The sender creates a one-time invitation link or QR code.
    
2. The recipient accepts the invitation.
    
3. Both devices establish independent encrypted message queues.
    
4. Messages are exchanged through SimpleX relay servers.
    
5. The relay servers forward encrypted messages but cannot determine who is communicating with whom.
    

```text
You
   ↓
Invitation Link / QR Code
   ↓
Encrypted Relay
   ↓
Encrypted Relay
   ↓
Recipient
```

Each conversation uses separate cryptographic identifiers, making it difficult to correlate multiple conversations to the same person.

## Privacy Features

| Feature                     | Support | Notes                                                                                           |
| --------------------------- | ------- | ----------------------------------------------------------------------------------------------- |
| Decentralized               | ⚠️      | Anyone can operate a relay server, but the network is federated rather than fully decentralized |
| Open source client          | ✅       | Android, iOS, Desktop, and CLI clients are open source                                          |
| Open source server          | ✅       | Relay server software is open source                                                            |
| End-to-end encryption       | ✅       | Enabled by default                                                                              |
| Forward secrecy             | ✅       | Uses modern cryptographic protocols that provide forward secrecy                                |
| Post-compromise security    | ✅       | Uses the Double Ratchet Algorithm for automatic key rotation and recovery                       |
| Metadata protection         | ✅       | No permanent user identifiers and separate queues reduce metadata exposure                      |
| Onion routing               | ❌       | Does not route messages through onion or mix networks                                           |
| No phone number required    | ✅       | No phone number is ever required                                                                |
| Anonymous signup            | ✅       | No account creation or email address required                                                   |
| Usernames                   | ❌       | Users are not identified by usernames or permanent IDs                                          |
| Multi-device support        | ⚠️      | Supported, though synchronization differs from traditional messaging apps                       |
| Independent security audits | ⚠️      | Protocol has received external review, though fewer audits than Signal                          |
| Cost                        | Free    | Donation supported                                                                              |

## What makes it different?

SimpleX takes a unique approach to private messaging by removing permanent user identifiers entirely.

Its distinguishing characteristics include:

- No phone numbers
    
- No usernames
    
- No email addresses
    
- No permanent accounts
    
- Every conversation uses unique identifiers
    
- Strong metadata protection
    
- Federated relay servers
    
- End-to-end encryption by default
    
- Open-source software
    
- Nonprofit development

## Main limitations

- Users must exchange invitation links or QR codes before communicating.
    
- Does not provide anonymous Internet routing like Tor or Nym.
    
- Smaller user base than mainstream messaging platforms.
    
- Multi-device support is less seamless than applications like Signal.
    
- Relay servers can observe that messages are being forwarded, even though they cannot read message contents or identify both ends of a conversation.