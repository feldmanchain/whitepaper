# feldmanchain, a decentralized network for building source code

__building the future of software, one bit at a time__

This is a (not even worth to be called) working draft where I keep notes and stuff like that while thinking about concepts, problems, solutions and more.

## Blockchain or not?

The more I think about it, implementing the feldmanchain as a blockchain (per the standard definition of it) almost feels like finding the problem to our solution. While a decentralized builder network shares _some_ characteristics of a blockchain, others just doesn't make sense. For example, a blockchain does a lot of things to keep the chain tamper proof, but we do not have to concern ourselves with that. When a build is done, it is done. There is no need for a history (that I can think of) and it might even be a potential vulnerability that could be easily avoided by omission.

I will look into other decentralized technologies to find inspiration, starting with the [bittorrent whitepaper](https://www.bittorrent.com/btt/btt-docs/BitTorrent_(BTT)_White_Paper_v0.8.7_Feb_2019.pdf) and reading up on the technical aspects of [git](https://git-scm.com/book/en/v2).

Having said that, I do like the game theory / incentivization that can be implemented within a blockchain, so it would be nice to somehow keep that aspect of it, were we to not implement this as a traditional blockchain.