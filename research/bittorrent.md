# BitTorrent

## The BitTorrent Protocol

[BitTorrent] runs on a protocol called the BitTorrent Protocol which is a distributed communication protocol created in 2001 by Bram Cohen. In some aspects it is a predecessor to blockchains, in that  there is no trusted third party and peers share information directly with each other, even though technically not a blockchain in its canonical form.

The main entity within the protocol is the client software endpoint (called a "client" or "peer"). Each peer in the network can both download files from other peers and upload files for other peers to download, eliminating the need for a central server.

To find a peer that has a file (or part of it), the network includes something called a "tracker" which is a server that keeps track of which peers has which files. This concept does sound like a form of centralization, but it is not a requirement for participation and there are alternatives such as doing a lookup in a decentralized database called the DHT. 

The files being transferred are cut into smaller pieces before being sent, each piece identified by a so called "info hash", making it possible to verify that the correct pieces are being transferred. Peers are naturally segmented into "swarms" by the common interest of sharing pieces of the same file. A client that is transferring pieces is regarded as productive, making the network favor it for further transfers, while less productive clients gets deprecated, disconnected or banned. A client is, however, not required to upload files to use the network.

There are several client that uses the BitTorrent protocol, the most famous being μTorrent.

## BTT (BitTorrent Token)

BitTorrent wants to enable the building of decentralized applications on their network, with the goal of being the infrastructure for the decentralized web. They seem to be well positioned to do this since they have the experience and infrastructure of running large, decentralized networks. They have identified blockchains as a paradigm shift in this space, and have therefore extended the BitTorrent protocol to encompass a blockchain with the native token BTT (BitTorrent Token). This solution provides a store of value and a means of exchange.

The main idea behind the blockchain seems to be for participants to exchange provision of (decentralized) infrastructure for token rewards, which, on the other end, allows businesses to use that infrastructure. On top of this, they plan to create a market place where participants can offer their infrastructure and/or sell goods and services for tokens. To put it plainly, as BitTorrent peer, you can lend out your computer for tokens, which you can later use to pay for goods and services.

## The BitTorrent blockchain / TRON

BitTorrent has partnered with a foundation called [TRON] that provides a blockchain ecosystem for building the decentralized web on. BitTorrent uses TRON to issue their TRC10 token (which is the TRON equivalent of a native token) BTT. To handle high volumes of transactions, it seems like they are running private off-chains which synchs to the public TRON blockchain.

## BitTorrent Speed

BitTorrent has expanded their protocol with an additional protocol called "Speed", which is layered on top of the old BitTorrent protocol and aims to ensure that peers does not disconnect before other peers are done downloading their files. The incentive for this is the BTT, which the downloading user can offer in exchange for being allowed to finish the download. 

## Establish a service request-and-provider relationship

When a peer makes a service request, it contains the max amount of BTT that the requester is willing to pay, which is followed by a bidding round. When a service provider wins the bid, an escrow account is established which holds the BTT transfer that be executed upon deliverance of the files.

How provider clients are chosen is dependant on their bids, but also upon another metric which is if the client is choked or not.

## Could we implement feldmanchain inside BitTorrent Speed

I found it interesting and fascinating that there is a large number of similarities between BitTorrent Speed and feldmanchain:

1. It identifies correctness of files using a cryptographic hash
1. It uses VCG auctions with an escrow account to settle bids
1. It implements an algorithm that auto-balances the cost of settling bids
1. It uses initial air drops to jump start the tokenonomy (though BT used investment schemes at a later stage)
1. It has the capabilities to fractionalize/distribute the sending of files (not sure how this would apply)

and on top of this, they are opening up the possibility to build dapps on their network.

I am not sure if it is possible to implement feldmanchain as a part of the BitTorrent speed network, given the specific needs that we have, but it is something that warrants further investigation, and if not, it will be very beneficial as something to help inform decisions, given how many similarities there are.


[TRON]: https://developers.tron.network/docs/getting-started
[BitTorrent]: https://www.bittorrent.com/btt/btt-docs/BitTorrent_(BTT)_White_Paper_v0.8.7_Feb_2019.pdf