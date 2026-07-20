## What is it?

Arweave is a decentralized storage network designed to preserve data permanently.

Users make a one-time payment to upload data, and the network rewards independent storage providers for keeping that data available over the long term.

Arweave describes itself as a global, permissionless hard drive for permanent information storage.

## Who created it?

Arweave was founded by [[Sam Williams]] and [[William Jones]].

Its mainnet launched in **2018**.

The protocol is open source and maintained by contributors across the Arweave ecosystem.

## Cost to use

Uploading data requires a one-time payment using the network’s native cryptocurrency, **AR**.

The price depends primarily on:

- The size of the data
    
- Current storage costs
    
- The price of AR
    
- Network conditions

Unlike [[Filecoin]] or traditional cloud storage, the user does not need to keep renewing a storage contract.

## How it works

Suppose you want to permanently store a document.

### 1. You upload the file

Your file is submitted as an Arweave transaction.

```text
Your file
   ↓
Arweave transaction
   ↓
Arweave network
```

The transaction contains:

- The data
    
- Metadata describing it
    
- Your signature
    
- A storage payment

### 2. The data enters the weave

Arweave stores transactions in a blockchain-like data structure historically called the **blockweave**.

Each new block is connected to earlier network history, creating a permanent, cryptographically verifiable record.

Your file becomes part of this shared historical dataset rather than being covered by a temporary storage contract.

### 3. Storage providers replicate the data

Independent Arweave nodes store portions of the network’s historical data.

A file is not stored on only one specific server. Multiple nodes may preserve and serve the same information.

```text
Your file
   ↓
Node A
Node B
Node C
```

### 4. Nodes prove access to old data

To participate successfully in the network, nodes must demonstrate access to randomly selected historical data.

Arweave currently uses **Succinct Proofs of Random Access**, or **SPoRA**, to reward nodes that can quickly access and serve data from the network’s history.

Conceptually:

```text
Network:
“Show that you can access this older piece of data.”

Node:
“Here it is, along with a valid proof.”
```

This encourages nodes to store broad portions of Arweave’s history rather than only the newest or most popular files.

## How permanent storage is funded

The most unusual part of Arweave is its **storage endowment**.

When someone pays to upload data:

```text
One-time storage payment
        ↓
Immediate miner reward
        +
Storage endowment
```

Part of the payment rewards storage providers immediately. The remainder supports an endowment intended to fund storage far into the future.

The model relies on the expectation that:

- Storage hardware becomes cheaper over time
    
- The upfront payment is conservatively priced
    
- Future storage costs can be covered from the endowment

Arweave therefore offers a protocol-level promise of permanent storage rather than requiring the original uploader to keep paying.

## What does “permanent” mean?

“Permanent” means the network is economically and technically designed to preserve data indefinitely after one payment.

It does not mean permanence is guaranteed by a law of nature.

The promise depends on:

- The Arweave network continuing to operate
    
- Enough nodes continuing to store historical data
    
- The endowment model remaining economically sustainable
    
- The protocol remaining secure
    
- People continuing to value and use the network

Arweave provides a stronger permanence commitment than temporary storage contracts, but it cannot literally guarantee that the network will exist forever.

## Retrieving data

Each uploaded item receives a transaction ID that can be used as a permanent address.

```text
Transaction ID
      ↓
Arweave gateway or node
      ↓
Retrieve and verify data
```

Users commonly access data through HTTP gateways.

For example, a gateway receives the transaction ID, retrieves the corresponding data from Arweave, and serves it through a normal web browser.

Gateways improve usability and performance, but relying on one gateway can reintroduce a centralized access point. The underlying data can still be retrieved through another gateway or directly from the network.

## The permaweb

The **permaweb** is the ecosystem of websites and applications stored on Arweave.

A web application can permanently store:

- HTML
    
- CSS
    
- JavaScript
    
- Images
    
- Application records
    
- Public datasets

Because its frontend files are stored permanently, the application does not depend entirely on one company continuing to pay a hosting bill.

Arweave supports an ecosystem of gateways, indexing services, bundlers, naming systems, and compute layers that make permanent data easier to use.

## Bundlers

Submitting every small file directly as its own base-layer transaction can be inefficient.

**Bundlers** collect many user uploads together and submit them to Arweave in larger batches.

```text
Small upload A ─┐
Small upload B ─┼→ Bundler → Arweave
Small upload C ─┘
```

Bundlers improve:

- Upload speed
    
- Payment convenience
    
- Support for very small files
    
- Developer experience

However, the bundler is an intermediary during upload. Users depend on it to successfully submit their data to the base network.

## AR token

**AR** is Arweave’s native cryptocurrency.

It is used for:

- Paying to store data
    
- Rewarding storage providers
    
- Transaction fees
    
- Supporting the storage endowment

Storage providers earn AR by maintaining data and participating in network consensus.

## Arweave and IPFS

Arweave and [[IPFS]] solve different problems.

|Technology|Main purpose|
|---|---|
|[[IPFS]]|Identify, verify, and distribute content|
|Arweave|Pay once to preserve content permanently|

IPFS says:

> Retrieve this exact content from any peer that has it.

Arweave says:

> Place this data into a network designed and funded to preserve it permanently.

With IPFS, someone must continue pinning the file.

With Arweave, continued storage is funded through the original payment and the network’s incentive system.

## Arweave and Filecoin

|Feature|[[Filecoin]]|Arweave|
|---|---|---|
|Payment model|Storage contract|One-time payment|
|Storage duration|Fixed period|Intended to be permanent|
|Renewal required|Yes|No|
|Provider selection|Client chooses providers|Network-wide incentive system|
|Storage proofs|Provider proves contracted sectors|Nodes prove access to historical data|
|Best suited for|Flexible bulk storage|Permanent public records|

Filecoin is closer to a decentralized storage marketplace.

Arweave is closer to a permanent public archive.

## AO

**AO** is a decentralized computing system built around Arweave’s permanent data layer.

It allows independent processes to:

- Run computations
    
- Exchange messages
    
- Maintain application state
    
- Use Arweave as a permanent record

Rather than making Arweave only a storage network, AO aims to support applications and autonomous processes whose messages and history can remain permanently verifiable. AO is currently live in an early mainnet phase.

## Common use cases

- Archiving public records
    
- Preserving websites
    
- NFT metadata and media
    
- Blockchain transaction history
    
- Journalism and censorship-resistant publishing
    
- Application frontends
    
- Academic datasets
    
- Historical and cultural archives
    
- Permanent audit logs
    
- Data used by decentralized applications

## What makes it different?

Arweave combines:

- One-time storage payments
    
- Permanent data commitments
    
- A storage endowment
    
- Permissionless storage providers
    
- Cryptographic verification
    
- Permanent application hosting
    
- A shared public data layer

Its primary goal is not cheap temporary storage. It is preserving information so that it remains available without depending on the original uploader.

## Main limitations

- Data generally cannot be deleted once permanently recorded.
    
- Users should encrypt private information before uploading it.
    
- Accidentally uploaded or illegal material may be extremely difficult to remove.
    
- The permanence promise depends on the network and economic model surviving.
    
- One-time storage can be more expensive upfront than temporary storage.
    
- Gateway dependence can introduce centralized access bottlenecks.
    
- Public data is accessible to anyone who knows or discovers its address.
    
- Permanent storage is unsuitable for information that may need to be corrected, withdrawn, or forgotten.
    
- The protocol’s economic assumptions have not yet been tested over centuries.

## Simple mental model

```text
IPFS:
“Who currently has this file?”

Filecoin:
“Pay these providers to store it until the contract ends.”

Arweave:
“Pay once to add it to a permanent public archive.”
```