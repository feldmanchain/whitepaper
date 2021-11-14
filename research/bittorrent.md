# BitTorrent

## The BitTorrent Protocol

[BitTorrent] runs on a protocol called the BitTorrent Protocol which is a distributed communication protocol created in 2001 by Bram Cohen. In some aspects it is a predecessor to blockchains, in that there is no trusted third party and the way peer discovery works. The main entity within the protocol is the client software endpoint (called a "client" or "peer"). Each peer in the network can both download/upload files from/to other peers, eliminating the need for a central server.

To find a peer that has a file (or part of it), the network utilizes two strategies. The first is a so-called distributed hash table (DHT) implemented as a "Kademlia" architecture, and the other is the concept of "trackers" which are servers that keeps track of which peers has which files. More or less all peer-to-peer networks, including blockchains, seem to use some variant of this architecture.

To exchange information, peers transfer files that are cut into smaller pieces before being sent, each piece identified by a so called "info hash", making it possible to verify that the correct pieces are being transferred. Peers are naturally segmented into "swarms" by the common interest of sharing pieces of the same file. A client that transfers information is regarded as productive, making the network favor it for further transfers, while less productive clients gets deprecated, disconnected or banned. A client is, however, not required to upload files to use the network.

There are several client that uses the BitTorrent protocol, the most famous being μTorrent.

## BitTorrent Speed

BitTorrent has expanded their protocol with an additional protocol called "Speed", which is layered on top of the old BitTorrent protocol and aims to ensure that peers do not disconnect before other peers are done downloading their files. The incentive for this is the BTT, BitTorrents new crypto, which the downloading user can offer in exchange for being allowed to finish the download. 

## The BitTorrent blockchain and BTT (BitTorrent Token)

BitTorrent has expanded their protocol to include a blockchain, including their crypto token BTT. The major use case for the blockchain seems to be for participants to exchange provision of (decentralized) infrastructure for token rewards, which, on the other end, allows businesses to use that infrastructure. On top of this, they plan to create a market place where participants can offer their infrastructure and/or sell goods and services for tokens. To put it plainly, as BitTorrent peer, you can lend out your computer for tokens, which you can later use to pay for goods and services.

BitTorrent has partnered with the [TRON] foundation that provides a blockchain ecosystem for building the decentralized web on. BitTorrent uses TRON to issue their TRC10 token (which is the TRON equivalent of a native token) BTT. To handle high volumes of transactions, it seems like they are running private off-chains which synchs to the public TRON blockchain.

## Establish a service request-and-provider relationship

When a peer makes a service request, it contains the max amount of BTT that the requester is willing to pay, which is followed by a bidding round. When a service provider wins the bid, an escrow account is established which holds the BTT transfer that should be executed upon deliverance of the files.

Provider clients are chosen based on their bids and another metric which is if the client is choked or not. How (un)chocked a client is is determined using a tit-for-tat algorithm based on (for example) how much data a client has received from a specific peer.

## Match-making and auctions

It seems like clients can implement any auction algorithm they want, but a Vickrey-Clarke-Groves is expected to be the optimum one. Since the files being requested are fragmented, n winning bids are picked, and the cost becomes the bid of the highest loosing bid.

## Payment and escrow accounts

To finalize transactions and payments, BTT implements a intermediary escrow account that continuously settles payments between the service requester and provider as fragments of the requested file is being transferred. The escrow account includes a timeout for each payment. If the fragment is not provided within the timeout the payment is cancelled and returned to the service requester. Likewise, if a service requester fails to follow through with the payment, it becomes choked, and potentially eventually banned from further requests.

## Common denominators between feldmanchain and BTT

There are some really interesting concepts in BTT that we could implement within feldmanchain. Here follows some of the applications.

### Exchange infrastructure for tokens

In many ways, BTT seems like a more generic version of the feldmanchain. Just like BTT, feldmanchain peers wants to lend out computer power in exchange for tokens, just in a more specific way.

### Allow the formations of swarms of peers

Peers that share a common interest to build certain projects (for example within a company) could be allowed to form swarms to do so. On top of the potential of increased security and performance, this could facilitate on-premise build networks, either on or off chain.

### Use (social) metrics to disincentivize bad faith actors

Both social and technical metrics could be implemented (and automated) to act as a form of prevention against harmful actions on the network. For example, builders that are shown to deliver bad builds, or that take a unproportionate long time to deliver build could receive a lower score than a performant and correct builder. This could potentially be used as a metric to take into account in the bidding process.

### Verify correctness using a cryptographic hash

As previously discussed, the correctness of a file (build) could be verified using a cryptographic hash.

### Use VCG auctions with an escrow account to settle bids

This, IMO, is a _super_ interesting idea that fits well into the concept of the feldmanchain. Although unaware of the formal definition of a VCG (or Vickrey) auction, I was already thinking along these lines. In feldmanchain we could use auctioneers to perform auctions and validations.

## Could we implement feldmanchain inside BTT?

I am not sure how, or even if, this is possible but given the large amount of similarities, I think further investigation into implementing feldmanchain as a decentralized application on BTT is warranted. On top of the commonalities pointed out above, BitTorrent has a large user base, a super strong networking layer and a secure execution environment.

[TRON]: https://developers.tron.network/docs/getting-started
[BitTorrent]: https://www.bittorrent.com/btt/btt-docs/BitTorrent_(BTT)_White_Paper_v0.8.7_Feb_2019.pdf