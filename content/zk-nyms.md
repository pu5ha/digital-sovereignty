## What are they?

zk-nyms are zero-knowledge credentials used within the [[Nym]] ecosystem.

They allow users to prove they have permission to use the network **without revealing who they are**.

For example, a user can prove:
- They have an active VPN subscription
- They paid for network access
- They possess a valid credential

without revealing their identity or creating a persistent account.

## Why do they exist?

Traditional VPNs require users to authenticate with:

- Email addresses
- Usernames
- Passwords
- API keys

This allows the VPN provider to associate activity with a specific customer.

zk-nyms remove that requirement.

Instead of proving **who you are**, users prove **that they have a valid credential**.

## How they work

A user purchases access to the Nym network.

Nym issues the user a cryptographic credential.

When connecting to the network, the user generates a **zero-knowledge proof** that demonstrates:

- "I possess a valid credential."

without revealing:

- Which credential
- Who purchased it
- Any identifying information

The network verifies the proof and grants access.

## Benefits

- No usernames or passwords
- No persistent accounts
- Prevents linking multiple sessions together
- Enables anonymous payments and authentication
- Reduces metadata collected by the provider

## Main limitation

zk-nyms hide user identity during authentication, but they do not replace the privacy guarantees provided by the [[Mixnets]] themselves.

They solve **authentication privacy**, whereas the mixnet protects **communication privacy**.