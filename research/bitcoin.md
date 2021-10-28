# Bitcoin

Bitcoin is the original crypto currency, created in 2009 by one or more person(s) under the pseudonym Satoshi Nakamoto. Even though it was the first that really gained traction, having solved the double-spend problem in a peer-to-peer network without a trusted third-party, just like all technological advancements it builds on prior work - such as Hashcash and b-money.

As stated above, Bitcoin is a trustless peer-to-peer network for making transactions between accounts. It uses the native token that goes under the same name as the blockchain itself - Bitcoin - as the underlying currency that gives the network value.

## Security

The trustless security of Bitcoin is derived from a couple of compounding factors, such as the economic incentives for the network participants (nodes) to not cause harm to the network, devaluing the network itself in doing so, and the computational impracticality for an attacker to overtake the network.

The way that the network is implemented is both simple and elegant. Transactions are finalized in so called blocks (hence the name blockchain). For a block to be added to the chain, it must be mined, which includes solving a computationally hard problem. The problem itself is dynamic in its complexity, varying depending on the average # of blocks mined per hour, automatically balancing the rate of mining.

Each node of the network stores a full<sup>1</sup> history of the network, and for the nodes to agree that a chain in the network is legit, more than 50% of the participants must agree on it. This way, if an attacker was to tamper with the chain, resulting in an alternative chain, he must overpower 50% of the CPU power of the entire chain to convince the network that his version is the correct one. This is very unlikely to say the least.

Since its launch Bitcoin has not been comprised a single time.

## Scaling

The computational complexity described above directly translates into time complexity, which has the side effect that it severely limits the number of transactions that can be processed within a given time. As you can see, this is by design; Bitcoin favors decentralization and security over performance. This problem is formalized as the "blockchain trilemma", where you can only pick two of the three above-mentioned characteristics.

Currently, Bitcoin handles up to 4.6 transactions per second, which is a rather low number compared to centralized solutions. There exists extensions to the Bitcoin blockchain that alleviates these issues, such  as the Lightning network that is a decentralized network of smart contracts on the Bitcoin blockchain itself that raises the transaction volumes and speeds by a large factor.

## Programmability

Bitcoin comes with a scripting language called Script, which is not turing complete, lacking loops, and intended to be used to describe simple transaction flows.

## Applicability to feldmanchain

I have a hard time seeing how we could benefit from using the Bitcoin chain in any capacity, since it is very specialized in solving a different set of problems then the feldmanchain is. There are extensions and bridges other than the Lightning network, like Thorchain, but those are mainly for interoperability and not something that would advance our cause.

_1. Because of how bitcoin is implemented, using a Merkle tree to represent the blocks in the chain, each node does not actually store the entire history of the bitcoin chain._