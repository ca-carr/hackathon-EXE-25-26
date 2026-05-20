# Game 1, The Offline Blockchain

## Game Overview
This game simulates a blockchain network **without computers or phones**, to get to the fundamental concepts through thinking about the actual interactions.

## Setup

We will split into groups of at least:
- 3 Verifier Groups (including Recorders)
- 1 Network Group (including Attackers)
- 2 Sender Groups

## Materials needed
- Pen(s)
- Paper
- A 6-sided [dice](https://www.random.org/dice/?num=1)
- Timer

# Initial Setup
- Decide on your groups: who will be the Sender group, the Verifier group, and the Network group.
- Each Sender group starts with 100 coins, assigned somehow (you decide)
- Create initial account balances on a "genesis block" (an initial state)
- All Verifier groups need to be aware of this state somehow (you decide)
- **Crucially,** before the game begins, all groups together decide how the blockchain system will work.

# Senders
The senders send transactions to the network.
- Write transactions on pieces of paper, fold them, and pass them to members of the Network group.
- You can decide on the transaction format; below are two examples to get you started.
```js
# example_1
id:  ...
to:  ...
from:  ...
amount:  ...
data:  ...
verification_information: ...
```
```js
# example_2
transaction #: ___
from: ___ (account)
to: ___ (account)
amount: ___ coins
time: ___
number: ___ (random number)
signature: ___
```


- Senders can send a maximum of 10 coins per transaction
- They must also record all that you send
- Sender groups start with 100 coins each, as per setup
- Sender groups will decide what initial accounts have any coins


## Sender Constraints
They can only communicate verbally with their own group and the Network group. They cannot speak with the Verifier groups.


## Senders' Goals

The senders' goals are quite easy to achieve.
- Each group must send over 100 coins in total to the other sender group.
- Each group must also include the names of their group members in different transactions, so that they are recorded as e.g. `name: M. Mifty, group: Sender-1` 

# Network and Attackers

- The Network group also contains the attackers. 
- The network takes transactions from both sender groups, reads them, and shows them to each of the Verifier groups.

The attackers are allowed to take the transaction paper out of the room (or otherwise hide it from view). In addition the attackers can:

1. write on the transaction paper
2. copy the transactions
3. create their own transactions (forgery)
4. delay transactions by up to one minute
5. reorder transactions

## Network Team Constraints

Before the game begins, only half the group is allowed to make attacker actions.

The members that are not attackers may leave the room, but may not manipulate transactions in the ways the attackers can.

- You must ensure you do not tell any other group who is an attacker and who is not. In addition, the Network group must act together.
- You must elect a recorder to record all the transactions that you see, and all of the attacker manipulated transactions.

## Network Team Goals

The first goal of the Network Team is to **deliver all transactions.**

In addition, the attacker members are aiming to achieve a couple of goals:

- Get the Recorder Team(s) to accept a double-spend
- Get the Recorder Team(s) to accept a forgery
- Make it so the ledger between the different recorder teams does not match
- Disrupt the system in any other way.


# Verifiers and Recorders

This group forms the consensus and agreement layer of the blockchain.

### Responsibilities
- Verify each transaction against the rules you decided.
- Accept or reject transactions.
- Update balances
- Append a transaction to your ledger
- When a new transaction is appended, roll the dice; on a 6, you have made a block.
    - Underscore transactions and share the block with the other groups
    - They must copy your ledger as it is and discard their own (though they may keep any transactions that they have not seen or have not been duplicated.)
- Flag suspicious transactions


## Recorder Team Goals
- Create more blocks than the other recorder teams.
- Detect and flag any tampered or invalid transactions.


# Game End and Win Conditions
- You have 10 minutes to decide on your blockchain system.
- The game ends after 20 minutes.
- Then there is a reconciliation system where we count the blocks created, and the number of attacker transactions that were included.


## Winning Criteria



### Network **Super Win** Condition:
- All blocks, or an overwhelming majority of blocks created, contain tampered or invalid transactions created by the attackers **and** the following win condition applies.

### Network **Win** condition:
- All transactions are delivered to all Recorder Teams on the network
- A forged transaction is included
- Cause inconsistency between recorded ledgers
- Cause invalid or double payment

### Recorders **Super Win** Condition: 
- More blocks created than other teams.
- No block contains tampered or invalid transactions created by the attackers.

### Recorders **Win** Condition:
- Created at least 2 blocks.
- The number of attacker transactions in your blocks is fewer than other recorders.

### Senders **Win** if:
- They send 100+ coins to the opposing team (or more)
- All transactions are accepted into the final blockchain.
- Each sender’s name appears at least once in accepted transactions.


---

# Debrief Questions
1. What made consensus difficult?
2. How did you detect fraudulent transactions?
3. What role did the block creation (mining) play?
4. How would digital signatures improve this system?
5. What happens when ledgers disagree?






