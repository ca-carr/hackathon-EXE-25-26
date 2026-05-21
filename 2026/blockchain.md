# Building a Blockchain Network

## The Challenge

Building the network infrastructure is one of the most challenging aspects of blockchain design.

In small groups, you are going to design and deploy your own (simple) blockchain network — one where nodes can communicate with peers, send transactions, and maintain a shared ledger. This is the digital version of what you explored in Game 1.

In the spirit of a hackathon, this is **not** a prescribed tutorial. Instead, you will decide how to build it.

---

## What You Need to Build

A minimal blockchain network has four core components. How you implement each one is up to you.

### 1. Peer-to-Peer (P2P) Network

Nodes need to find each other and pass messages around the network.

**Things to consider:**
- How does a new node discover existing nodes?
- What happens when a node goes offline?
- How do you forward a message without duplicating it forever?

At a minimum, your network should be able to:
- Connect two or more nodes together
- Send a message from one node and have it received by another

### 2. Transactions

Transactions are the data being exchanged. They need to be structured so that any node can read and validate them.

**Things to consider:**
- What fields does a transaction need? (sender, receiver, amount, a unique ID?)
- How do you prevent someone from sending coins they don't have?
- How do you prevent someone from replaying the same transaction twice?

A minimal transaction might look something like:

```
from:   <address>
to:     <address>
amount: <value>
id:     <unique identifier>
```

But you can design your own format.

### 3. Blocks and the Chain

How are you going to create your blockchain?

**Things to consider:**
- How many transactions go in a block? Is 1 ok?
- What links one block to the previous one?
- What stops someone from altering old blocks?

A minimal block might contain:
- A list of transactions
- A reference to the previous block 
- Some kind of identifier

### 4. Verification and Storage

Nodes need to agree on which transactions and blocks are valid, and they need to store the chain somewhere.

**Things to consider:**
- What makes a transaction invalid?
- What makes a block invalid?
- Where do you store the chain?
- What happens when two nodes have different versions of the chain?

---

## Getting Started

You are free to use any language or tools available to you. Python is a reasonable choice, but the decision is yours.

Some starting points to think about before writing any code:

1. **Sketch the message format** — what does a transaction look like as data you'd send over a network?
2. **Sketch the block format** — what does a block look like?
3. **Decide on transport** — how will nodes talk to each other? How can you achieve it? 
4. **Start small** — get two nodes talking before worrying about chains and consensus.

---

## Goals

These are the milestones to aim for, roughly in order of difficulty:

1. **Get your network running** — at least two nodes connected and able to exchange messages.
2. **Send and receive a transaction** — one node creates a transaction, another receives and validates it.
3. **Connect with another group's network** — get a node from your network to connect to someone from another group, or connect to their network.

---

## Things to Watch Out For (Advanced Items)

These are the same problems you encountered in Game 1, now in code:

- **Double-spending** — can someone send the same coins twice before the network catches it?
- **Forgery** — can someone create a transaction on behalf of another address?
- **Inconsistent state** — what happens when two nodes accept conflicting transactions?
- **Message flooding** — if every node forwards every message, how do you stop the network from looping?

You do not need to solve any / all of these. But be aware of them, and be ready to discuss where your design is vulnerable.

---

## Debrief Questions

1. What design decisions did you make early on that you later had to change?
2. Where in your system would an attacker have the easiest time causing problems?
3. How did you handle disagreement between nodes?
4. How does your implementation compare to what you experienced in the offline game?
