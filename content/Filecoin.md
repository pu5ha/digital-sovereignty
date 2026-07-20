## What is it?

Filecoin is a decentralized network where users pay independent storage providers to store data for an agreed period.

It combines:

- A storage marketplace
    
- Cryptographic proofs
    
- A blockchain
    
- The FIL cryptocurrency

Unlike [[IPFS]], Filecoin creates economic incentives for someone to keep storing your data.

## Who created it?

Filecoin was created by [[Protocol Labs]] and proposed by [[Juan Benet]].

Its mainnet launched in **October 2020**.

## Cost to use

Storage is not automatically free.

The price depends on factors such as:

- How much data is stored
    
- How long it is stored
    
- Which provider is selected
    
- How many copies are stored
    
- Retrieval requirements

Users and storage providers negotiate storage agreements in an open marketplace. Payments and collateral use the network’s native token, **FIL**.

## How it works

Suppose you have a file already identified by an IPFS CID:

```text
bafyMovie123
```

### 1. You choose a storage provider

You find a Filecoin storage provider willing to store the file.

The provider offers terms such as:

```text
Store 100 GB
For 12 months
For a certain price
```

You can make deals with several providers if you want multiple independent copies.

### 2. You create a storage deal

The agreement specifies:

- Which data must be stored
    
- The storage provider
    
- The price
    
- The storage period
    
- The cryptographic commitment to the data

The actual negotiation may happen off-chain, while the resulting storage commitment is recorded through the Filecoin network.

### 3. The provider receives the data

The storage provider transfers the data onto its own storage hardware.

Filecoin providers organize data into standardized containers called **sectors**. Current sector sizes include 32 GiB and 64 GiB.

```text
Your file
   ↓
Storage provider
   ↓
Filecoin sector
   ↓
Provider's hard drives
```

### 4. The provider seals the sector

The provider performs a computation called **sealing**.

Sealing creates a unique encoded copy of the sector tied to that particular provider.

The provider then submits a **Proof-of-Replication**, showing that it created a unique physical copy of the data rather than merely claiming to store it.

### 5. The provider continuously proves storage

Storing the file once is not enough.

Throughout the deal, the Filecoin network challenges the provider to prove that the data is still being stored.

The provider responds with **Proof-of-Spacetime**:

```text
Filecoin network:
“Prove you still possess this data.”

Storage provider:
“Here is a cryptographic proof.”
```

These proofs can only be generated reliably if the provider still has the sealed data.

### 6. The provider earns FIL

When the provider submits valid proofs, it can:

- Receive storage payments
    
- Earn network rewards
    
- Maintain its pledged collateral

Providers must lock FIL as collateral. If they fail to prove storage, they can lose rewards or collateral.

## How retrieval works

When you want the file back, you request it using:

- Its CID
    
- Its storage-deal information

A provider holding the data sends it back to you. The file itself is stored off-chain; the blockchain tracks commitments, deals, and proofs rather than storing the full file.

```text
You request CID
      ↓
Find provider storing it
      ↓
Provider sends the data
      ↓
CID verifies the file
```

Storage and retrieval are related but separate services. A provider may be good at long-term storage without necessarily offering fast retrieval.

## Filecoin and IPFS

IPFS and Filecoin solve different problems.

|Technology|Main purpose|
|---|---|
|[[IPFS]]|Identify, verify, and distribute content|
|[[Filecoin]]|Pay providers and prove that content remains stored|

IPFS says:

> Get the content matching this CID from anyone who has it.

Filecoin adds:

> Pay these providers to keep that content and require them to prove they still have it.

Filecoin does not require every stored file to be continuously available through the public IPFS network, although the two systems commonly use compatible CIDs and tooling.

## Key concepts

### Storage providers

Storage providers operate the hardware that stores user data.

They supply:

- Disk capacity
    
- Bandwidth
    
- Computing power for proofs
    
- Collateral

Anyone can participate, but operating competitively generally requires specialized hardware, technical expertise, and significant capital.

### Storage deals

A storage deal is an agreement between a user and a provider.

It defines:

- The data
    
- Price
    
- Duration
    
- Provider
    
- Storage commitment

A deal lasts for a fixed period. Data is not guaranteed to remain stored after the deal expires unless it is renewed or copied elsewhere.

### Sectors

A sector is the basic unit of provable storage within Filecoin.

A sector may contain:

- One large piece of client data
    
- Several smaller pieces
    
- Unused padding

Filecoin generates proofs around the sector rather than submitting a separate blockchain proof for every individual file.

### Proof-of-Replication

Proof-of-Replication demonstrates that a provider created its own unique encoded copy of the data.

This helps prevent a provider from pretending one copy satisfies several separate storage commitments.

### Proof-of-Spacetime

Proof-of-Spacetime demonstrates that the provider continued storing the data over time.

Providers submit these proofs repeatedly throughout the storage period.

### FIL

FIL is Filecoin’s native cryptocurrency.

It is used for:

- Storage payments
    
- Provider collateral
    
- Network rewards
    
- Transaction fees
    
- Smart-contract activity

## Filecoin Virtual Machine

The **Filecoin Virtual Machine**, or **FVM**, allows smart contracts to run on Filecoin.

Developers can use it to create applications involving:

- Automated storage deals
    
- Data-access rules
    
- Storage subscriptions
    
- Provider financing
    
- Programmable data markets

The FVM runs computation and manages commitments, while the large files remain stored off-chain by providers.

## What makes it different?

Filecoin combines decentralized storage with enforceable economic commitments.

Its defining features include:

- Permissionless storage marketplace
    
- Independent storage providers
    
- Fixed-duration storage deals
    
- Cryptographic proof that data remains stored
    
- Provider collateral and penalties
    
- Compatibility with content-addressed data
    
- Programmable storage through the FVM

## Main limitations

- Filecoin does not make storage permanent; deals expire.
    
- Users should store multiple copies with different providers for stronger redundancy.
    
- Fast retrieval is not guaranteed merely because data is stored.
    
- Storage providers are often professional data-center operators rather than ordinary home users.
    
- Sealing and proof generation require substantial computation and specialized hardware.
    
- Files are not private by default and should be encrypted before storage when confidentiality matters.
    
- Using Filecoin directly can be technically complex, so many users rely on applications or intermediary services.
    
- The blockchain proves that providers hold committed data, but it does not guarantee that every provider will offer a convenient user experience.

## Simple mental model

```text
IPFS
“Here is the fingerprint and structure of my file.”

Filecoin
“I will pay providers to store it, and they must continually prove that they still have it.”
```