## What it is

Tor is a free, open-source anonymity network. It routes internet traffic through multiple independently operated relays so that no single relay should know both who the user is and where they are connecting.

Its main products are the Tor network, [[Tor Browser]], onion services, and censorship-circumvention tools such as bridges.

https://www.youtube.com/watch?v=QRYzre4bf7I
## Who maintains it

Tor’s software is primarily developed and coordinated by [[The Tor Project, Inc.]], a US 501(c)(3) nonprofit founded in 2006.

The network itself is not operated solely by the Tor Project. Most Tor relays and bridges are run by independent volunteers and organizations that donate servers and bandwidth.

## Cost to use?

It is free! Tor Browser and the Tor network are free to use.

There is no subscription, token, or payment required. The Tor Project says its tools are funded without collecting, selling, or renting user data.

## Is it a public good?

Yes. Tor is best understood as digital public infrastructure.

It is:

- Open source
    
- Free at the point of use
    
- Available globally
    
- Maintained by a nonprofit and contributor community
    
- Supported by volunteer-run infrastructure
    
- Designed to provide privacy and censorship resistance rather than generate profit
    

It is not perfectly decentralized, because the Tor Project coordinates core development and a small set of directory authorities helps establish the accepted list of relays. But operation of the network is distributed across thousands of independent relay operators.

## Main limitation

Tor provides stronger anonymity than directly connecting or using a normal proxy, but it is slower, frequently blocked by websites, and remains vulnerable to some traffic-correlation attacks by sufficiently powerful observers.

## How Tor Works

When you connect to a website normally:

You → ISP → Website

The ISP knows who you are and where you're going. The website knows your IP address.

With Tor:

You → Guard Relay → Middle Relay → Exit Relay → Website

Before sending any traffic, your Tor client selects three relays and establishes an encrypted session with each using its public key.

Your request is then encrypted three times:

1. Encrypted with the Exit relay's public key
2. Wrapped again with the Middle relay's public key
3. Wrapped again with the Guard relay's public key

As the packet moves through the network:

- **Guard relay** removes the outer encryption layer using its private key. It knows your IP address but only learns the next relay.
- **Middle relay** removes the next layer. It only knows the previous and next relay.
- **Exit relay** removes the final layer and sends the request to the destination website. It knows the destination but not your IP address.

Because each relay only decrypts one layer, no single relay knows both who you are and where you're going.

The website sees the Exit relay's IP address instead of yours, while your ISP only sees that you're connected to the Tor network—not which website you're visiting.