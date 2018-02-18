
(Mk II) CrocodileCash Official Re-Development Repo
==================================================

*** To be changed to something with a similar purpose ***
[![Build Status](https://travis-ci.org/peercoin/peercoin.svg?branch=master)](https://travis-ci.org/peercoin/peercoin)
*** end to-be-changed ***


### What is (future) CrocodileCash?
[CrocodileCash](www.croccash.com / www.crocodilecash.ga) (abbreviated CROC), is a cryptocurrency originally developed in August 2017 featuring a hybrid Sha256 Proof-of-Work and a 12% annual Proof-of-Stake.  We have rebased the code using the most current version of Peercoin (PPC) [https://github.com/peercoin/peercoin], instead of the older codebase of AntiBitcoin (ANTI) [https://github.com/antibitcoin/AntiBitcoin-source] that CROC was originally forked from.

## Original characteristics of this beast (seeking to keep these approximately the same)

Algorithm: SHA-256 PoW/DPOS/PoS Hybrid

Block Time: 30 Seconds

Difficulty Re-targeting: Every Block

Total Coins: 55,000,000 (55 Million)

Pre-Mine: 302,400 Coins (Half for Developer & the Rest for Bounties + Giveaway)

PoW Reward: 15 coins per block until block 80640 (1 Month) then 1 coin per block afterwards

DPOS: 1st Week = 60 coins (Starts at block 1440)

2nd Week = 45 coins

3rd Week = 30 coins

4th Week = 15 coins (Ends at block 80640)

PoS Yearly Interest: 12% Yearly Interest (Starts at block 80641) (1 Month)

Minimum Stake Age: 2 hours

Maximum Stake Age: Unlimited

Mined Block Confirmations Require: 60 Blocks

Transaction Confirmations Require: 20 Blocks

RPC Port: 39438

P2P Port: 39437

CrocodileCash.conf


## Roadmap for this variant

Seeking to perform a 1:1 coin swap of the old CROC to this more modern and streamlined version before the old coin supply exceeds 3,300,000 CROC.  We want to pre-announce this and allow sufficient lead-time for holders, mining pools, and exchanges to move to this new chain.

To incentivize users (of the earlier form of this chain) to adopt this new one, we plan to reinstate a substantially-similar Distributed Proof-of-Stake period (such that holders of the old coin will end up with a greater proportion of the current stake in the new chain). 

We plan to reduce the block sizes from the extremely large (for a cryptocurrency) 20 MB to 750 kB (or 1 MB ???)

We plan to put hardwired seed nodes into the code.

Checkpoints will become more frequent.


[...]



Testing
-------



*** Possibly to be removed ***

### Automated Testing

Developers are strongly encouraged to write unit tests for new code, and to
submit new unit tests for old code.

Unit tests can be compiled and run (assuming they weren't disabled in configure) with:
  make check

Every pull request is built for both Windows and Linux on a dedicated server,
and unit and sanity tests are automatically run. The binaries produced may be
used for manual QA testing — a link to them will appear in a comment on the
pull request posted by [BitcoinPullTester](https://github.com/BitcoinPullTester). See https://github.com/TheBlueMatt/test-scripts
for the build/test scripts.

### Manual Quality Assurance (QA) Testing

Large changes should have a test plan, and should be tested by somebody other
than the developer who wrote the code.

* Developers work in their own forks, then submit pull requests when they think their feature or bug fix is ready.
* If it is a simple/trivial/non-controversial change, then one of the development team members simply pulls it.
* If it is a more complicated or potentially controversial change, then the change may be discussed in the pull request, or the requester may be asked to start a discussion in the [Peercoin Forum](https://talk.peercoin.net) for a broader community discussion. 
* The patch will be accepted if there is broad consensus that it is a good thing. Developers should expect to rework and resubmit patches if they don't match the project's coding conventions (see coding.txt) or are controversial.
* From time to time a pull request will become outdated. If this occurs, and the pull is no longer automatically mergeable; a comment on the pull will be used to issue a warning of closure.  Pull requests closed in this manner will have their corresponding issue labeled 'stagnant'.
* For development ideas and help see [here](https://talk.peercoin.net/c/protocol).

## Branches:

### develop (all pull requests should go here)
The develop branch is used by developers to merge their newly implemented features to.
Pull requests should always be made to this branch (except for critical fixes), and could possibly break the code.
The develop branch is therefore unstable and not guaranteed to work on any system.

### master (only updated by group members)
The master branch get's updates from tested states of the develop branch.
Therefore, the master branch should contain functional but experimental code.

### release-* (the official releases)
The release branch is identified by it's major and minor version number e.g. `release-0.6`.
The official release tags are always made on a release branch.
Release branches will typically branch from or merge tested code from the master branch to freeze the code for release.
Only critical patches can be applied through pull requests directly on this branch, all non critical features should follow the standard path through develop -> master -> release-*

*** end possibly-to-be-removed ***
