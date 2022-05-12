# Awesome Move [![Awesome](https://awesome.re/badge.svg)](https://awesome.re)

> A curated list of code and content from the [Move](https://github.com/move-language/move) programming language community.

Move is a programming language for writing safe smart contracts originally developed at Facebook to power the Libra blockchain. Move is designed to be a platform-agnostic language to enable common libraries, tooling, and developer communities across diverse blockchains with vastly different data and execution models. Move's ambition is to become the "JavaScript of web3" in terms of ubiquity--when developers want to quickly write safe code involving assets, it should be written in Move.

## Contents

- [Overview](#overview)
- [Move-Powered Blockchains](#move-powered-blockchains)
- [Books](#books)
- [Tutorials](#tutorials)
- [Community](#community)
- [Code](#code)
  - [Fungible Tokens](#fungible-tokens)
  - [Non-Fungible Tokens](#non-fungible-tokens)
  - [DeFi](#defi)
  - [On-Chain Governance](#on-chain-governance)
  - [Accounts](#accounts)
  - [Frameworks](#frameworks)
  - [Libraries](#libraries)
  - [Miscellaneous](#miscellaneous)
- [Tools](#tools)
- [IDEs](#ides)
- [Wallets](#wallets)
- [Papers](#papers)
  - [Language Design](#language-design)
  - [Static Analysis and Verification](#static-analysis-and-verification)
- [Videos](#videos)

## Overview

- [Installation](https://github.com/move-language/move/tree/main/language/tools/move-cli#installation)
- [Problem Statement](docs/problem_statement.md)

## Move-Powered Blockchains

- [Sui](https://github.com/MystenLabs/sui) (in [devnet](https://medium.com/mysten-labs/sui-devnet-public-release-a2be304ff36b))
- [0L](https://github.com/OLSF/libra) (in [mainnet](https://0l.network/))
- [Starcoin](https://github.com/starcoinorg/starcoin) (in [mainnet](https://stcscan.io/))
- [Aptos](https://github.com/aptos-labs/aptos-core) (in [devnet](https://aptos.typeform.com/to/jwSOZbH6))
- [Pontem](https://github.com/pontem-network) (in [testnet](https://polkadot.js.org/apps/?rpc=wss://testnet.pontem.network/ws#/explorer))
- [Aptos](https://github.com/aptos-labs) (in [devnet](https://aptos.dev/))
- [Celo](https://github.com/celo-org) ([coming soon](https://www.businesswire.com/news/home/20210921006104/en/Celo-Sets-Sights-On-Becoming-Fastest-EVM-Chain-Through-Collaboration-With-Mysten-Labs))
- [Diem](https://github.com/diem/diem)

## Books

- https://diem.github.io/move/ - Maintained by the Move core team.
- https://move-book.com/ - Maintained by [@damirka](https://github.com/damirka).

## Tutorials

- [Implementing, testing, and verifying a fungible token](https://github.com/move-language/move/tree/main/language/documentation/tutorial) - Maintained by the Move core team.

## Community

- [Move @ Mysten Labs Discord](https://discord.gg/M95qX3KnG8)
- [Move Language Discord](https://discord.gg/9K7ca8Vnr7)
- [Move @ 0L Discord](https://discord.gg/zzXzhbE3aN)
- [Move @ Starcoin Discord](https://discord.gg/starcoin)

## Code

Code written in Move.

### Fungible Tokens

- [BasicCoin](https://github.com/move-language/move/tree/main/language/documentation/examples/experimental/basic-coin) - A toy implementation of an [ERC20](https://ethereum.org/en/developers/docs/standards/tokens/erc-20/)-like fungible token.
- [Diem](https://github.com/OLSF/libra/blob/main/language/diem-framework/modules/Diem.move) - An ERC20-like token with permissioned minting/burning, see also this [spec](https://github.com/diem/dip/blob/main/dips/dip-20.md). Deployed on 0L.
- [Token](https://github.com/starcoinorg/starcoin-framework/blob/main/sources/Token.move) - Another ERC20-like Token. Deployed on Starcoin.
- [GAS](https://github.com/OLSF/libra/blob/main/language/diem-framework/modules/0L/GAS.move) - A token that instantiates the Diem standard above. Deployed on 0L.
- [STC](https://github.com/starcoinorg/starcoin-framework/blob/main/sources/STC.move) - A token that instantiates the Starcoin standard above. Deployed on Starcoin.
- [WEN stablecoin](https://github.com/wenwenprotocol/wen-protocol) - Deployed on Starcoin.
- [FAI stablecoin](https://github.com/BFlyFinance/FAI) - Deployed on Starcoin.
- [FLY stablecoin](https://github.com/BFlyFinance/FLY) - A fork of [Ohm](https://www.olympusdao.finance/) implemented in Move. Deployed on Starcoin.
- [Synthetic token backed by a basket containing a reserve of other tokens](https://github.com/OLSF/libra/blob/main/language/diem-framework/modules/XDX.move) - From Diem.

### Non-Fungible Tokens

- [NFT](https://github.com/starcoinorg/starcoin-framework/blob/main/sources/NFT.move) - An ERC721-like token. Deployed on Starcoin.
- [Merkle Airdrop](https://github.com/starcoinorg/starcoin-framework/blob/main/sources/MerkleNFT.move) - Utility for airdropping a large number of NFT's. Deployed on Starcoin.
- [NFT](https://github.com/diem/diem/blob/main/diem-move/diem-framework/experimental/sources/NFT.move) - An implementation of a hybrid ERC721/ERC1155-like token. From Diem.
- [BARS](https://github.com/diem/diem/blob/main/diem-move/diem-framework/experimental/sources/BARS.move) - An NFT that instantiates this hybrid standard. From Diem.
- [MultiToken](https://github.com/diem/diem/blob/main/diem-move/diem-framework/experimental/sources/MultiToken.move) - An ERC1155-like token. From Diem.
- [NFTGallery](https://github.com/diem/diem/blob/main/diem-move/diem-framework/experimental/sources/NFTGallery.move) - Utility for holding multiple NFT's of the same type. From Diem.

### DeFi

- [CoinSwap](https://github.com/move-language/move/tree/main/language/documentation/examples/experimental/coin-swap) - A toy implementation of a [Uniswap](https://uniswap.org/)-like liquidity pool containing two tokens.
- [StarSwap](https://github.com/Elements-Studio/starswap-core) - A Uniswap-style DEX. Deployed on Starcoin.
- [Offer](https://github.com/move-language/move/blob/main/language/move-stdlib/nursery/sources/Offer.move) - Generic implementation of atomic swaps for any pair of assets.

### On-Chain Governance

- [ValidatorUniverse](https://github.com/OLSF/libra/blob/main/language/diem-framework/modules/0L/ValidatorUniverse.move) - Validator set management. Deployed on 0L.
- [Oracle](https://github.com/OLSF/libra/blob/main/language/diem-framework/modules/0L/Oracle.move) - For on-chain community voting. Deployed on 0L.
- [DAO](https://github.com/starcoinorg/starcoin-framework/blob/main/sources/Dao.move) - For on-chain proposals and voting. Deployed on Starcoin.
- [DiemSystem](https://github.com/diem/diem/blob/main/diem-move/diem-framework/DPN/sources/DiemSystem.move) - Validator set management. From Diem.
- [Vote](https://github.com/diem/diem/blob/main/diem-move/diem-framework/experimental/sources/Vote.move) - On-chain voting. From Diem.

### Accounts

- [Account](https://github.com/diem/diem/blob/main/diem-move/diem-framework/core/sources/Account.move) - A generic account for Diem-powered chains. From Diem.
- [DiemAccount](https://github.com/OLSF/libra/blob/main/language/diem-framework/modules/DiemAccount.move) - Fork of the above. From 0L.
- [Account](https://github.com/starcoinorg/starcoin-framework/blob/main/sources/Account.move) - Fork of the above. From Starcoin.

### Frameworks

A Move **framework** is the set of Move modules included in the genesis state of the chain. 
These modules typically implement key concepts like accounts, currencies, . 
The ability to separate blockchain-specific framework logic from the generic functionality of the Move language is a key part of Move's platform-agnostic design.

- [Diem Framework](https://github.com/diem/diem/tree/main/diem-move/diem-framework/DPN)
- [0L Framework](https://github.com/OLSF/libra/tree/main/language/diem-framework/modules/0L)
- [Starcoin Framework](https://github.com/starcoinorg/starcoin-framework)

### Libraries

- [Move standard library](https://github.com/move-language/move/tree/main/language/move-stdlib) - Utilities intended (but not required) to be used in every platform running Move. From the Move repo.
- [Move nursery](https://github.com/move-language/move/tree/main/language/move-stdlib/nursery) - Experimental modules that may eventually be promoted into the standard library. From the Move repo.
- [Decimal](https://github.com/OLSF/libra/blob/main/language/diem-framework/modules/0L/Decimal.move) - Efficient implementation of a decimal value. From 0L.
- [Math](https://github.com/starcoinorg/starcoin-framework/blob/main/sources/Math.move) - Math utility functions. From Starcoin.
- [Compare](https://github.com/move-language/move/blob/main/language/move-stdlib/nursery/sources/Compare.move) - Polymorphic comparison (i.e., compare any two Move values of the same type). From the nursery.
- [Vault](https://github.com/move-language/move/blob/main/language/move-stdlib/nursery/sources/Vault.move) and [ACL](https://github.com/move-language/move/blob/main/language/move-stdlib/nursery/sources/ACL.move) - Libraries for capability and list-based acess control. From the nursery.
- [TaoHe](https://github.com/taoheorg/taohe) - A collection of nestable Move resources.
- [Starcoin Framework Commons](https://github.com/starcoinorg/starcoin-framework-commons) - Libraries for Move commons utility on starcoin-framework. From Starcoin.

### Miscellaneous

- [Move-on-EVM](https://github.com/move-language/move/tree/main/language/evm/examples) - Experimental examples for the project to compile Move source code to EVM bytecode.

## Tools

- [Move Package Manager](https://github.com/move-language/move/tree/main/language/tools/move-cli) - Like `cargo` or `npm` for Move: single CLI (and corresponding Rust API's for other tools to hook into) for building, running, testing, debugging, and verifying Move [packages](https://diem.github.io/move/packages.html). Maintained by the Move core team.
- [Move Prover](https://github.com/move-language/move/tree/main/language/move-prover) - Formal verification of user-defined specifications written in Move source code. Maintained by the Move core team.
- [Move Read/Write Set Analyzer](https://github.com/move-language/move/tree/main/language/tools/read-write-set) - Static analysis tool for computing an overapproximation of the global memory touched by a Move program. Maintained by the Move core team.

## IDEs

- Move vscode plugin ([install](https://marketplace.visualstudio.com/items?itemName=move.move-analyzer), [source code](https://github.com/move-language/move/tree/main/language/move-analyzer)) - Maintained by the Move core team.
- Move syntax vscode plugin: context-based Move syntax highlighting ([install](https://marketplace.visualstudio.com/items?itemName=damirka.move-syntax), [source code](https://github.com/damirka/vscode-move-syntax)) - Maintained by [@damirka](https://github.com/damirka).
- Move IntelliJ plugin ([install](https://plugins.jetbrains.com/plugin/14721-move-language), [source code](https://github.com/pontem-network/intellij-move))
- [Move Playground](https://playground.pontem.network/) - Like [Remix](https://remix.ethereum.org/) for Move--alpha version of a Web IDE. See [instructions](https://gist.github.com/borispovod/64b6d23741d8c1f4b0b958a3a74aa68d). Maintained by the Pontem team.

## Wallets

- StarMask ([install](https://chrome.google.com/webstore/detail/starmask/mfhbebgoclkghebffdldpobeajmbecfk?hl=en), [source code](https://github.com/starcoinorg/starmask-extension)) - A wallet for the Starcoin blockchain. Maintained by the Starcoin team.
- [bcs-js](https://github.com/pontem-network/lcs-js) - JavaScript implementation of the [BCS](https://github.com/diem/bcs) serialization scheme used by Move, may be useful for implementing wallets.

## Papers

### Language Design

- [Move: A Language With Programmable Resources](https://developers.diem.com/papers/diem-move-a-language-with-programmable-resources/2019-06-18.pdf) - This was the original Move white paper released in 2018. Many aspects of this are now out of date (e.g., the syntax and description of the bytecode instructions), but the first two sections are worth a read for explaining the difficulties of programming with assets and how Move tackles them.
- [Robust Safety for Move](https://arxiv.org/abs/2110.05043)
- [The Move Borrow Checker](https://arxiv.org/abs/2205.05181)
- [Resources: A Safe Language Abstraction for Money](https://arxiv.org/abs/2004.05106)

### Static Analysis and Verification

- [Fast and Reliable Formal Verification of Smart Contracts with the Move Prover](https://arxiv.org/abs/2110.08362)
- [The Move Prover](https://research.facebook.com/publications/the-move-prover/)
- [Verification of Programs Written in Libra's Move Language](https://ethz.ch/content/dam/ethz/special-interest/infk/chair-program-method/pm/documents/Education/Theses/Constantin_M%C3%BCller_MS_Report.pdf)
- [Exact and Linear-Time Gas-Cost Analysis](https://research.facebook.com/publications/exact-and-linear-time-gas-cost-analysis/)

## Videos

- [Move: A Safe Language for Programming with Money](https://www.youtube.com/watch?v=EG2-7bQNPv4&ab_channel=FieldsInstitute) - Talk from [@sblackshear](https://github.com/sblackshear) at the [Fields Institute Blockchain](http://www.fields.utoronto.ca/activities/seminar_series/blockchain-research-seminar-series) research seminar series.
- [Formal Verification of Move Programs for the Libra Blockchain](http://www.fields.utoronto.ca/talks/Formal-verification-Move-programs-Libra-blockchain) - Talk from [@DavidLDill](https://github.com/DavidLDill) at the [Fields Institute Blockchain](http://www.fields.utoronto.ca/activities/seminar_series/blockchain-research-seminar-series) research seminar series.

## Contributing

Contributions welcome! Read the [contribution guidelines](CONTRIBUTING.md) first.
