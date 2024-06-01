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

**Ethereum Hashing:**
- Ethereum uses its own hashing algorithm, Keccak-256, which is similar to SHA-256 and belongs to the SHA family.
- For our purposes, we focus on the concept of hashing.

**Hashing Process:**
- Any data entered into the data section of the application is processed by the SHA-256 hash algorithm, resulting in a unique hash.
- No matter the input size, the generated hash string's length remains constant.

### Understanding Blocks

Now that we understand hashing and fixed-length strings, let's look at the structure of a blockchain—a collection of blocks.

**Block Structure:**
- A block contains three parts: block number, nonce, and data.
- All three parts are processed through the hash algorithm to produce the hash for that block.
- Even a minor change in the data results in an entirely different hash, invalidating the block.

**Mining:**
- Mining involves finding a nonce that produces a hash following a specific pattern, such as starting with four zeros.
- This process involves computational trial and error.
- The criteria a miner must solve varies between blockchains, but the concept remains the same.

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

If a single entity controlled the blockchain, they could change data and re-mine subsequent blocks, compromising security.

**Decentralization:**
- Blockchain's power lies in its decentralized nature.
- Multiple entities (peers) run the blockchain technology, each with equal power.
- In case of tampering, the majority hash wins, as agreed upon by the network.
- Nodes that disagree with the majority fork the network, continuing with their own history.

### Interplay of Blockchain & Transactions

- The data in a block can be anything, not just random text.
- In token and coinbase sections, each block comprises multiple transactions hashed together.
- Any edits to transactions invalidate the chain.

### Conclusion

- Every transaction, block, and the entire blockchain itself relies on the concept of a hash—a unique fixed-length string linked to the original data.
- Decentralization and immutability are key to blockchain's security.
- Understanding hashing and block structure is fundamental to grasping how blockchain technology works.
