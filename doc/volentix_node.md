---
abstract: |
  The Volentix token, VTX was originally created on the main EOSIO
  chain. The Volentix network is a network of voting nodes which run
  software to support the volentix ecosystem: Staking, Proposals and
  Wrapping of VTX on EOS/Ethereum.
author:
- |
  Sylvain Cormier\
  `sylvain@volentixlabs.com`
title: Volentix network v0.0.1
---

Introduction 
============

The Volentix network is a docker network using a .yml file for
configuration.

System
======

1.  **Docker network**\

    1.  An oracle script constantly feeding an EOS contract with the ETH
        VTX balance, account name, timestamp, and block info\* (disabled
        in this version )

    2.  OpenEthereum

    3.  Bitcoin

    4.  EOS

    5.  Volentixnode  

        1.  Voting

        2.  Distribution

        3.  Signing (Disabled in this version)

2.  **Registration**\
    User chooses jobs:

    1.  Voting system(mandatory)

    2.  Oracle

3.  **EOS contracts**  

    1.  Staking

    2.  Custodian

    3.  Token

    4.  Pool

    5.  Gateway

centering ![](vltxnode.png "fig:"){#fig:whitebackground-ecosystem02}

Conditions
==========

1.  EOS custodian must be must be updated continuously by a minimum of 8
    oracles.

2.  No oracle can submit its value twice.

3.  Sources must register to the Volentix node network.

4.  Users must be able to pick the work/rewards they do.

5.  Volentix nodes should be extended with new functionality of being
    able to update without having to null registrations.

6.  Nodes must have 10000 VTX staked.
