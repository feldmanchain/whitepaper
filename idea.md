# Trustless and predictable bidding using Vickrey auctions and consensus through discrete uniform build distributions

## TLDR

_I suggest we use a second-price closed-envelop (Vickrey or Vickrey–Clarke–Groves) auction to handle build requests with an auctioneer/validator escrow intermediary to settle auctions, validate builds and execute payouts. I further suggest that we use a distributed consensus mechanism with a discrete uniform distribution over n auctioneers and builders to prevent coordinated attacks._

_Much like other blockchains, security and integrity is achieved by decentralization. Even if a single validator or builder acts in bad faith, given sufficient decentralization, a coordinated attack should be statistically impossible._

## Solving the problem of gaming the system

With regards to the system we are building, and the services it provides, we can assume that it is in the interest of the participants to be able to reason about and predict the cost and/or rewards associated with their respective tasks within the system. It is also reasonable to assume that the users want strong guarantees in regards to safety, trust and reliability.

To build confidence in the system (which is trustless by design) we must prove to our users that it is indeed safe, reliable and predictable. This is a multifaceted problem, but one that is solved by other blockchains in part or in whole and/or more broadly within game theory.

## Use cases (in regards to the above statements)

1. As a project author, I want to make build requests
    * I want to pay fair compensation for the work
    * I want strong guarantees that the build output is bona fide (authentic, genuine)
1. As a builder, I want to carry out build requests
    * I want to be fairly compensated for my work
    * I want a fair and equal chance to be selected when bidding on a build request
1. As an auctioneer, I want to facilitate build request auctions
    * I want to be fairly compensated for my work
    * I want a fair and equal chance to be selected when bidding on a build request
1. As a validator, I want to validate the correctness of builds
    * I want to be fairly compensated for my work
    * I want a fair and equal chance to be selected when bidding on a build request

## Identifying the weak points

As we can see, the builders, auctioneers and validators are different types of service providers in the network and therefore share the same goal which is to perform a task, and receive compensation for it. The end users (project authors) have slightly different needs since they are the only real service requester and the ones paying for the service to be executed.

Disregarding the end user for the moment, let's reason about the differences amongst the service providers in the network. In the interest of first optimizing for correctness before regarding things such as performance, let's think about how each of them could try to manipulate the system, and potential solutions.

Since we do not rely on a trusted third party, the mechanisms to prevent bad actors must be able to exist in a decentralized network.

Within the scope of these issues, we will not discuss (equally important) aspects such as integrity, 

## Solution

Some of these use cases and problems will not be directly addressed within this part of the system, but I argue that most will be directly or indirectly solved or mitigated within the proposed system.


### discrete uniform distribution

`k = 1/n`

System defined base fee up to a total of T. Users can add extra to be prioritized

can the different network participants validate each other?

Fair launch, to coin drop