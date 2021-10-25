# Ethereum 

_After having read the whitepaper, I must say that the way Ethereum is designed is quite ingenious and was probably quite revolutionary at the time._

Ethereum is the first widely adopted general-purpose programmable blockchain. Founded by Vitalik Buterin and with the help of minds like Gavin Wood (Polkadot) and Charles Hoskinson (Cardano), it is the most popular layer one blockchain today. It has seen great success in areas such as defi, NFTs and decentralized organisations, but does have it's issues when it comes to scaling in regards to transaction speed and cost, which has caused a lot of layer two technologies to build on ethereum.

At the time of writing, and at its conception, it is/was what is referred to as a second generation blockchain, which practically means that it uses proof of work as a consensus mechanism, but offer programability. Ethereum is currently in the processes of rolling out what is called layer two scaling, which includes things such as proof of stake, sharding and more. This will effectively make it a third generation blockchain, which tends to be more energy-efficient and that scales better.

One of Ethereums design goals is "Universality", as they aim to make it possible to build any program on top of it. Per that definition it _should_ be technically possible to implement the feldmanchain as one or more smart contracts. It might be the case that we would not be able to provide the adequate level of privacy, but that would have to be researched.

Furthermore, Ethereum takes modularity (which is another of their design goals) very seriously. While good in the context of a general-purpose, decentralized block chain, that could make it more cumbersome to implement the feldmanchain.

## Accounts

Ethereum uses different types of accounts as the main entities that lives on the chain. There are two type of accounts; __externally owned accounts__, which acts much like a personal bank account and __contract accounts__ which is small autonomous programs that executes logic. Owned accounts and contracts can communicate via messages and transactions. 

## Transactions and code execution

Ethereum contracts executes transactions and messages. In order to do so, the sender is required to pay a fee (gas) per operation the contract executes as well as for every byte sent. This is a mechanic that acts as a protection against attackers. You are also required to pay a base transaction fee that provides an insentive (a tip) to the node validators. The fee is spent even if the transaction fails.

## Code execution environment

As per the Ethereum whitepaper, code is executed by all nodes that validates the node containing the code.

> the process of executing contract code is part of the definition of the state transition function, which is part of the block validation algorithm, so if a transaction is added into block B the code execution spawned by that transaction will be executed by all nodes, now and in the future, that download and validate block B.

Not sure if this is something we want. We probably want a build to be built once and only once.

## Applications

The three types of applications suited for Ethereum, as they describe it themselves are __financial applications__, __semi financial applications__ and __decentralized governance__, none of which our system fits well into.

## Other

Concepts such as tokens, identity, reputation, decentralized autonomous organisations, decentralized file storage, time or event-triggered self-executing contracts and much more are things that can be built on Ethereum. Most of these do not apply to feldmanchain.

## Tokenomics

I won't go into the tokenomics of Ethereum, but it should be noted that applications running on and/or integrating with Ethereum stand a higher chance to be adopted since there is an added network effect and further monetary insentives.

## pros

### 1. Already implemented, production-tested etc

Implementing feldmanchain on Ethereum would alleviate us from having to build a blockchain of our own. Having said that, much of what is built within Ethereum, such as programmability and the code execution environment (the EVM) does not apply to a potential feldmanchain.

### 2. A large eco system, with lots of documentation

As mentioned earlier, the network effect of running on Ethereum would probabl only be positive.

### 3. Existing infrastructure running validator nodes

Could we somehow integrate the source code builders into validator nodes on Ethereum,that would be massive. Not sure how that would happen unless integrated into the nodes themselves, which is _very_ unliely to happen to say the least.

## cons

### 1. Cost

As described in the section [Transactions and code execution](#transactions-and-code-execution), you pay per operation executed and byte sent, both likely to be of a large quantity within the context of building source code. __The cost of hosting the feldmanchain within Ethereum is probably the biggest blocker__, even with future scaling solutions being implemented.

### 2. Bloat

The ethereum chain has a lot of governing mechanics / game mechanis that makes a lot of sense within the context of securing a publically available, fully decntralized, general-purpose programmable blockchain, but not so much within a blockchain with the single purpose of building source code. I foresee these being cumbersome and potential blockers.

### 3. Limited control

By definition, running our system on another platform limits our control. This is true for any third-party solution though.

### 4. Self-hosting

Since one of our top goal is to be able to provide the feldmanchain as an on-prem solution, we would need to be able to set up mini instances of ethereum in an intranet. This is probably possible, but that is not what Ethereum was built for.
