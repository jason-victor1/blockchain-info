# Understanding Hash Functions and Blockchain

This readme provides a detailed explanation of hash functions, blockchain structure, mining, immutability, decentralized distribution, and the interplay of blockchain and transactions.

## Table of Contents

1. [Understanding Hash Functions](#understanding-hash-functions)
2. [Understanding Blocks](#understanding-blocks)
3. [The Inherent Beauty of Blockchain: Immutability](#the-inherent-beauty-of-blockchain-immutability)
4. [Decentralized Distribution](#decentralized-distribution)
5. [Interplay of Blockchain & Transactions](#interplay-of-blockchain--transactions)
6. [Conclusion](#conclusion)

### Understanding Hash Functions

At its simplest, a hash is a unique, fixed-length string that identifies any piece of data. When you input any data into a hash function, it produces a hash. In this demo, we focus on the SHA-256 hash algorithm.

**Example:**
- If we input "Jason Victor" into the SHA-256 algorithm:
  - The letters are converted to numbers.
  - The numbers are then converted to a fixed-length string, or hash.
  - "Jason Victor" gets converted to: `845f8505e0759e003bf24c24109798384067415d3a8650fa2e51adc1cc3cd379`. Please see screen shot below.

![Hash](https://github.com/jason-victor1/blockchain-info/blob/main/hash%20function.png?raw=true)

## Ethereum Hashing

Ethereum employs the **Keccak-256 hashing algorithm** which is a cryptographic hash function from the **Keccak family**. This produces a fixed 256-bit hash. It was selected as the basis for **SHA-3** by NIST in 2012 and is widely used in blockchain applications like Ethereum for ensuring data integrity and generating addresses.

### Key Features of Keccak-256

- **Input-Independent Length:** Accepts messages of any length but outputs a fixed 256-bit hash.
- **Secure Properties:** Resistant to collisions and preimage attacks which ensures robust cryptographic security.
- **Deterministic:** The same input always generates the same hash which makes it predictable for verification purposes.
- **Efficient and Robust:** It Guarantees an avalanche effect. This is where even small changes in the input produce significantly different outputs.

We will focus on the concept of hashing with Keccak-256 being a cornerstone of Ethereum's security and reliability.

**Hashing Process:**
- Any data entered into the data section of the application is processed by the SHA-256 hash algorithm which will result in a unique hash.
- The generated hash string's length remains constant no matter the input size.

### Understanding Blocks

We understand hashing and fixed-length strings so now let's look at the structure of a blockchain—a collection of blocks.

**Block Structure:**
- A block contains three parts: block number, nonce, and data.
- All three parts are processed through the hash algorithm to produce the hash for that block.
- Even a minor change in the data results in an entirely different hash which invalidates the block.

**Mining:**
- Mining involves finding a nonce that produces a hash following a specific pattern such as starting with four zeros.
- This process involves computational trial and error.
- The criteria a miner must solve varies between blockchains but the concept remains the same.

### The Inherent Beauty of Blockchain: Immutability

**Blockchain Structure:**
- A blockchain is a sequence of blocks, each containing:
  - Block number
  - Nonce
  - Data
  - Hash of the previous block

**Immutability:**
- Any changes to data in a block invalidate every subsequent block until they are recalculated or re-mined.
- **Genesis Block:** The first block in a blockchain.

### Decentralized Distribution

If a single entity controlled the blockchain, then they could change data and re-mine subsequent blocks. As a result, this would compromise security.

**Decentralization:**
- Blockchain's power lies in its decentralized nature.
- Multiple entities (peers) run the blockchain technology. Each has equal power.
- In case of tampering, the majority hash wins which is agreed upon by the network.
- Nodes that disagree with the majority fork the network. This continues with their own history.

### Interplay of Blockchain & Transactions

- The data in a block can be anything, not just random text.
- In token and coinbase sections, each block comprises multiple transactions hashed together.
- Any edits to transactions invalidate the chain.

### Conclusion

- Every transaction, block, and the entire blockchain itself relies on the concept of a hash—a unique fixed-length string linked to the original data.
- Decentralization and immutability are key to blockchain's security.
- Understanding hashing and block structure is fundamental to grasping how blockchain technology works.
