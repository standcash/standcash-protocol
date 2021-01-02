# Stand Cash

[![Twitter Follow](https://img.shields.io/twitter/follow/standcash?label=Follow)](https://twitter.com/standcash)
[![License](https://img.shields.io/github/license/Stand-cash/standcashprotocol)](https://github.com/Stand-Cash/standcash-protocol/blob/master/LICENSE)
[![Coverage Status](https://coveralls.io/repos/github/Stand-Cash/standcash-protocol/badge.svg?branch=master)](https://coveralls.io/github/Stand-Cash/standcash-protocol?branch=master)

Stand Cash is a lightweight implementation of the [Stand Protocol](stand.io) on Ethereum. 

## The Stand Cash Protocol

Stand Cash differs from the original Stand Project in several meaningful ways: 

1. **Rationally simplified** - several core mechanisms of the Stand protocol has been simplified, especially around bond issuance and seigniorage distribution. We've thought deeply about the tradeoffs for these changes, and believe they allow significant gains in UX and contract simplicity, while preserving the intended behavior of the original monetary policy design. 
2. **Censorship resistant** - we launch this project anonymously, protected by the guise of characters from the popular SciFi series Rick and Morty. We believe this will allow the project to avoid the censorship of regulators that scuttled the original Stand Protocol, but will also allow Stand Cash to avoid founder glorification & single points of failure that have plagued so many other projects. 
3. **Fairly distributed** - both Stand Shares and Stand Cash has zero premine and no investors - community members can earn the initial supply of both assets by helping to contribute to bootstrap liquidity & adoption of Stand Cash. 

### A Three-token System

There exists three types of assets in the Stand Cash system. 

- **Stand Cash ($SAC)**: a stablecoin, which the protocol aims to keep value-pegged to 1 US Dollar. 
- **Stand Bonds ($SAB)**: IOUs issued by the system to buy back Stand Cash when price($SAC) < $1. Bonds are sold at a meaningful discount to price($SAC), and redeemed at $1 when price($SAC) normalizes to $1. 
- **Stand Shares ($SAS)**: receives surplus seigniorage (seigniorage left remaining after all the bonds have been redeemed).

### Stability Mechanism

- **Contraction**: When the price($SAC) < ($1 - epsilon), users can trade in $SAC for $SAB at the SABSAC exchange rate of price($SAC). This allows bonds to be always sold at a discount to cash during a contraction.
- **Expansion**: When the price($SAC) > ($1 + epsilon), users can trade in 1 $SAB for 1 $SAC. This allows bonds to be redeemed always at a premium to the purchase price. 
- **Seigniorage Allocation**: If there are no more bonds to be redeemed, (i.e. bond Supply is negligibly small), more $SAC is minted totalSupply($SAC) * (price($SAC) - 1), and placed in a pool for $SAS holders to claim pro-rata in a 24 hour period. 

Read the official [Stand Cash Documentation](docs.stand.cash) for more details.

## Motivation

We, the core developers of Stand Cash, were early supporters & observers of Stand when it first launched, and to this day believe that it is one of the best ideas to have ever been put forward in crypto. While Bitcoin first got us interested in blockchain's use cases, it was Stand that first truly inspired us, by painting a picture of a world that runs entirely on decentralized digital dollars the policies for which cannot be corrupted or politicized. Stand is more relevant now today than it ever was in 2017/2018 - with regulators striking back against the decentralized movement by cracking down on Telegram and Libra, while their governments are printing money faster than ever before in human history. 

This is not a DeFi project. We are simply leveraging the industry's excitement in the category to bring much deserved attention and engagement to the Stand Protocol, and to use this opportunity to distribute ownership in the protocol fairly.

Our only motivation is to bring the Stand Protocol into the world, and to serve its community in implementing Stand' vision to become the first widely adopted decentralized dollar. To that end, we are committed to take no financial upside in Stand Cash's success - we will raise no money and premine no tokens. Instead, when we feel that the protocol has found reasonable product market fit, we will ask the Stand Shares DAO for donations to keep contributing to the protocol. 

## How to Contribute

To chat with us & stay up to date, join our [Telegram](https://t.me/standcash).

Contribution guidelines are [here](./CONTRIBUTING.md)

For security concerns, please submit an issue [here](https://github.com/Stand-Cash/standcash-contracts/issues/new).


_© Copyright 2020, Stand Cash_
