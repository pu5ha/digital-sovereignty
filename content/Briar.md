## What is it?

Briar is a free, open-source messaging application designed for people who need resilient, censorship-resistant communication.

Unlike most messaging apps, Briar can communicate directly between devices whenever possible. When an Internet connection is unavailable or blocked, it can also synchronize messages over **Bluetooth** or **Wi-Fi**, allowing communication to continue during Internet outages.

Briar is designed for journalists, activists, humanitarian workers, and anyone who needs secure communication in environments where networks may be monitored, censored, or unavailable.

## Who maintains it?

Briar is developed by the **[[Briar Project]]**, a nonprofit organization dedicated to building secure and resilient communication tools.

The software is open source and developed by contributors from around the world.

## Cost to use?

Briar is completely free to use.

There are no advertisements, subscriptions, or premium features.

## Is it a public good?

Yes.

Briar is open source, developed by a nonprofit organization, and focused on protecting freedom of communication rather than generating profit.

## How it works

Briar takes a different approach from most messaging apps.

Whenever possible, devices communicate directly using the **Tor network**, avoiding centralized messaging servers.

If the Internet is unavailable, Briar can instead synchronize messages using:

- Bluetooth
    
- Local Wi-Fi

Messages are stored on users' devices until they can be delivered.

```text
You
   ↓
Tor
   ↓
Recipient

or

You
   ↓
Bluetooth / Wi-Fi
   ↓
Recipient
```

This allows conversations to continue even during Internet shutdowns or censorship.

## Privacy Features

| Feature                     | Support | Notes                                                              |
| --------------------------- | ------- | ------------------------------------------------------------------ |
| Decentralized               | ✅       | No central messaging servers                                       |
| Open source client          | ✅       | Android application is open source                                 |
| Open source server          | N/A     | Briar uses peer-to-peer communication rather than servers          |
| End-to-end encryption       | ✅       | Enabled by default                                                 |
| Forward secrecy             | ✅       | Uses modern cryptographic protocols                                |
| Post-compromise security    | ✅       | Uses the Double Ratchet Algorithm                                  |
| Metadata protection         | ✅       | No central server storing communication metadata                   |
| Onion routing               | ✅       | Internet communication is routed through Tor                       |
| No phone number required    | ✅       | No phone number or email required                                  |
| Anonymous signup            | ✅       | No account creation                                                |
| Usernames                   | ❌       | Contacts are added by exchanging invitation links or QR codes      |
| Multi-device support        | ❌       | Each device is independent                                         |
| Independent security audits | ⚠️      | Protocol has received external review but fewer audits than Signal |
| Cost                        | Free    | Donation supported                                                 |

## What makes it different?

Briar is unique because it continues working even when traditional messaging infrastructure is unavailable.

Its distinguishing characteristics include:

- Peer-to-peer communication
    
- No central messaging servers
    
- Built-in Tor integration
    
- Offline messaging via Bluetooth and Wi-Fi
    
- No phone numbers or accounts
    
- Strong metadata protection
    
- Open-source software
    
- Nonprofit development
    

Rather than depending on cloud infrastructure, Briar prioritizes resilience and censorship resistance.

## Main limitations

- Currently only available on Android.
    
- Contacts must be added in person or through trusted invitation links.
    
- Offline messaging only works when devices are physically close enough for Bluetooth or local Wi-Fi.
    
- Peer-to-peer communication may be slower or less reliable than cloud-based messaging services.
    
- Smaller user base than mainstream messaging applications.
    
- Does not currently offer seamless multi-device synchronization.