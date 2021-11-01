# BitTorrent

## The BitTorrent Protocol

BitTorrent runs on a protocol called the BitTorrent Protocol which is a distributed communication protocol created in 2001 by Bram Cohen. In some aspects it is a predecessor to blockchains, in that  there is no trusted third party, but peers sharing information with each other. It is not a block chain in its original form though.

The main entity within the protocol is the client software endpoint (called a "client" or "peer"). Each peer in the network can both download files from other peers or upload files for other peers to download, eliminating the need for a central server.

To find a peer that has a file (or part of it), the network includes something called a "tracker" which is a server that keeps track of which peers has which files. This concept does sound like a form of centralization, but it is not a requirement for participation and the exists alternatives such as doing a lookup in a decentralized database called the DHT. 

The files being transferred are cut into smaller pieces before being sent, each piece identified by a so called "info hash", making it possible to verify that the correct pieces are being transferred. Peers are naturally segmented into "swarms" by the common interest of sharing pieces of the same file. A client that is transferring pieces is regarded as productive, making the network favor it for further transfers, while less productive clients gets deprecated, disconnected or banned. A client is, however, not required to upload files to use the network.

There are several client that uses the BitTorrent protocol, the most famous being μTorrent.

## BTT (BitTorrent Token)

BItTorrent wants to enable the building of decentralized applications on their network, with the goal of being the infrastructure for the decentralized web. They seem to be well positioned to do this since they have the experience and infrastructure of running large, decentralized networks. They have identified blockchains as a paradigm shift in this space, and have therefore extended the BitTorrent protocol to encompass a blockchain with the native token BTT (BitTorrent Token). This solution provides a store of value and a means of exchange.

The main idea behind the blockchain seems to be for participants to exchange provision of (decentralized) infrastructure for token rewards, which, on the other end, allows businesses to use that infrastructure. On top of this, they plan to create a market place where participants can offer their infrastructure and/or sell goods and services for tokens. Plainly, as BitTorrent peer, you can lend out your computer for tokens, which you can later use to pay for goods and services.

## The BitTorrent blockchain

BitTorrent has partnered with a blockchain platform called the TRON foundation for building their cryptographic token BTT. To handle high volumes of transactions, it seems like they are running private off-chains which synchs to the public TRON blockchain.