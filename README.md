<!--lint disable double-link-->
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
  - [Decentralized Identity](#decentralized-identity)
  - [DeFi](#defi)
  - [SocialFi](#socialfi)
  - [On-Chain Governance](#on-chain-governance)
  - [Cross-Chain Bridge](#cross-chain-bridge)
  - [Accounts](#accounts)
  - [Frameworks](#frameworks)
  - [Libraries](#libraries)
  - [Miscellaneous](#miscellaneous)
- [Tools](#tools)
- [IDEs](#ides)
- [Package Managers](#package-managers)
- [Wallets](#wallets)
- [SDKs](#sdks)
- [Papers](#papers)
  - [Language Design](#language-design)
  - [Static Analysis and Verification](#static-analysis-and-verification)
- [Videos](#videos)
- [Slides](#slides)
- [Podcasts](#podcasts)
- [Blog Posts](#blog-posts)
- [Security](#security)

## Overview

- [Installation](https://github.com/move-language/move/tree/main/language/tools/move-cli#installation)
- [Problem Statement](https://github.com/mystenlabs/awesome-move/blob/main/docs/problem_statement.md#problem-statement)

## Move-Powered Blockchains

- [Sui](https://github.com/MystenLabs/sui) - A next-generation smart contract platform with high throughput, low latency, and an asset-oriented programming model powered by the Move programming language (in [devnet](https://medium.com/mysten-labs/sui-devnet-public-release-a2be304ff36b)).
- [0L](https://github.com/OLSF/libra) - A reference implementation of a neutral replicated state machine. Forked from the Libra/Diem technologies (in [mainnet](https://0l.network/)).
- [Starcoin](https://github.com/starcoinorg/starcoin) - A smart contract blockchain network that scales by layering (in [mainnet](https://stcscan.io/)).
- [Aptos](https://github.com/aptos-labs/aptos-core) - Aptos-core strives towards being the safest and most scalable layer one blockchain solution (in [mainnet](https://explorer.aptoslabs.com/?network=mainnet)).
- [Pontem](https://github.com/pontem-network/pontem) - Substrate based parachain with MoveVM onboard (in [testnet](https://polkadot.js.org/apps/?rpc=wss://testnet.pontem.network/ws#/explorer)).
- [Celo](https://github.com/celo-org/celo-blockchain) - Blockchain with EVM and MoveVM ([coming soon](https://www.businesswire.com/news/home/20210921006104/en/Celo-Sets-Sights-On-Becoming-Fastest-EVM-Chain-Through-Collaboration-With-Mysten-Labs)).
- [Diem](https://github.com/diem/diem) - The original Move based blockchain from Meta (form. Libra by Facebook) (discontinued).
- [ChainX](https://github.com/chainx-org/ChainX) - Bitcoin's layer2 smart contract network has already supported WASM and EVM, and is supporting MoveVM (in [mainnet](https://scan.chainx.org)).

## Books

- [Move Book](https://move-language.github.io/move/) - Move book maintained by the Move core team ([中文](https://github.com/move-language/move/tree/main/language/documentation/book/translations/move-book-zh)).
- [Move Book](https://move-book.com/) - Move book maintained by [@damirka](https://github.com/damirka) ([中文](https://move-book.com/cn/)).
- [Move Patterns](https://www.move-patterns.com/) - A book on Move software design patterns maintained by [@villesundell](https://github.com/villesundell).
- [Sui Move by Example](https://examples.sui.io/) - A book on the Sui Move variant maintained by [@MystenLabs](https://github.com/MystenLabs).

## Tutorials

- [Implementing, testing, and verifying a fungible token](https://github.com/move-language/move/tree/main/language/documentation/tutorial) - Maintained by the Move core team.
- [Programming with objects](https://docs.sui.io/build/programming-with-objects) - Maintained by the Sui team.
- [Move and SmartContract Development](https://starcoinorg.github.io/starcoin-cookbook/docs/move/) - Maintained by the Starcoin team.
- [Move Language](https://imcoding.online/courses/move-language) - Interactive Move language course, free for everyone, maintained by [imcoding.online](https://imcoding.online) ([中文](https://imcoding.online/courses/move-language?lng=zh)).

## Community

- [Move Language Discord](https://discord.gg/cPUmhe24Mz)
- [Move @ Sui by Mysten Labs Discord](https://discord.gg/sui)
- [Move @ 0L Discord](https://discord.gg/0lnetwork)
- [Move @ Starcoin Discord](https://discord.gg/starcoin)
- [Move @ Aptos Discord](https://discord.gg/aptoslabs)
- [MoveChina](https://move-china.com) - The largest Chinese community for the Move programming language.

## Code

Code written in Move.

### Fungible Tokens

- [Fungible token examples](https://github.com/MystenLabs/sui/tree/main/sui_programmability/examples/fungible_tokens) - Multiple example token implementations from Sui.
- [BasicCoin](https://github.com/move-language/move/tree/main/language/documentation/examples/experimental/basic-coin) - A toy implementation of an [ERC20](https://ethereum.org/en/developers/docs/standards/tokens/erc-20/)-like fungible token.
- [Diem](https://github.com/OLSF/libra/blob/main/language/diem-framework/modules/Diem.move) - An ERC20-like token with permissioned minting/burning, see also this [spec](https://github.com/diem/dip/blob/main/dips/dip-20.md). Deployed on 0L.
- [Token](https://github.com/starcoinorg/starcoin-framework/blob/main/sources/Token.move) - Another ERC20-like Token. Deployed on Starcoin.
- [GAS](https://github.com/OLSF/libra/blob/main/language/diem-framework/modules/0L/GAS.move) - A token that instantiates the Diem standard above. Deployed on 0L.
- [STC](https://github.com/starcoinorg/starcoin-framework/blob/main/sources/STC.move) - A token that instantiates the Starcoin standard above. Deployed on Starcoin.
- [STAR](https://github.com/Elements-Studio/starswap-core/blob/master/sources/gov/STAR.move) - A governance token of Starswap dApp that powers the AMM+DEX ecosystem. Deployed on Starcoin.
- [XUSDT](https://github.com/Elements-Studio/poly-stc-contracts/blob/master/sources/asset/erc20/XUSDT.move) - A mapped assets of USDT on Starcoin.
- [XETH](https://github.com/Elements-Studio/poly-stc-contracts/blob/master/sources/asset/erc20/XETH.move) - A mapped assets of ETH on Starcoin.
- [WEN stablecoin](https://github.com/wenwenprotocol/wen-protocol) - Deployed on Starcoin.
- [FAI stablecoin](https://github.com/BFlyFinance/FAI) - An over-collateralized stable coin deployed on Starcoin.
- [FLY stablecoin](https://github.com/BFlyFinance/FLY) - An implementation of forked OHM that deployed on Starcoin.
- [Synthetic token backed by a basket containing a reserve of other tokens](https://github.com/OLSF/libra/blob/main/language/diem-framework/modules/XDX.move) - From Diem.
- [XBTC](https://github.com/OmniBTC/OmniBridge/blob/main/aptos/bridge/sources/xbtc.move) - BTC mirror asset on Aptos.
- [XBTC](https://github.com/OmniBTC/OmniBridge/blob/main/sui/bridge/sources/xbtc.move) - BTC mirror asset on Sui.

### Non-Fungible Tokens

- [NFT examples](https://github.com/MystenLabs/sui/tree/main/sui_programmability/examples/nfts) - Multiple NFT example implementations from Sui.
- [NFT](https://github.com/starcoinorg/starcoin-framework/blob/main/sources/NFT.move) - An ERC721-like token. Deployed on Starcoin.
- [Merkle Airdrop](https://github.com/starcoinorg/starcoin-framework/blob/main/sources/MerkleNFT.move) - Utility for airdropping a large number of NFTs. Deployed on Starcoin.
- [NFT](https://github.com/diem/diem/blob/main/diem-move/diem-framework/experimental/sources/NFT.move) - An implementation of a hybrid ERC721/ERC1155-like token. From Diem.
- [BARS](https://github.com/diem/diem/blob/main/diem-move/diem-framework/experimental/sources/BARS.move) - An NFT that instantiates this hybrid standard. From Diem.
- [MultiToken](https://github.com/diem/diem/blob/main/diem-move/diem-framework/experimental/sources/MultiToken.move) - An ERC1155-like token. From Diem.
- [NFTGallery](https://github.com/diem/diem/blob/main/diem-move/diem-framework/experimental/sources/NFTGallery.move) - Utility for holding multiple NFT's of the same type. From Diem.
- [NFT Protocol](https://github.com/Origin-Byte/nft-protocol) - NFT protocol and collection framework. From OriginByte.
- [Suia](https://github.com/Mynft/suia) - The first POAP application on Sui.

### Decentralized Identity
- [aptos-cid](https://github.com/coming-chat/aptos-cid) - Decentralized identity on Aptos, the underlying account system of ComingChat.
- [MoveDID](https://github.com/NonceGeek/MoveDID) - MoveDID is a DID protocol that compatible with Move-based blockchain networks, including Aptos, Sui, and Starcoin. Maintained by the [NonceGeek](https://github.com/NonceGeek).


### DeFi

- [DeFi examples](https://github.com/MystenLabs/sui/tree/main/sui_programmability/examples/defi) - Multiple DeFi example implementations from Sui.
- [CoinSwap](https://github.com/move-language/move/tree/main/language/documentation/examples/experimental/coin-swap) - A toy implementation of a [Uniswap](https://uniswap.org/)-like liquidity pool containing two tokens.
- [Starswap](https://github.com/Elements-Studio/starswap-core) - A Uniswap-style DEX. Deployed on Starcoin.
- [Offer](https://github.com/move-language/move/blob/main/language/move-stdlib/nursery/sources/offer.move) - Generic implementation of atomic swaps for any pair of assets.
- [AptosRedPacket](https://github.com/coming-chat/aptos-red-packet) - A red packet social app that combines private chat and encrypted wallet on Aptos.
- [SuiRedPacket](https://github.com/coming-chat/sui-red-packet) - A red packet social app that combines private chat and encrypted wallet on Sui.
- [AptosAMMswap](https://github.com/OmniBTC/Aptos-AMM-swap) - Aptos AMM Swap implemented by the OmniBTC team.
- [SuiAMMswap](https://github.com/OmniBTC/Sui-AMM-swap) - Sui AMM Swap implemented by the OmniBTC team.
- [AptosOmniSwap](https://github.com/OmniBTC/OmniSwap/tree/main/aptos) - One-click swap between aptos and EVM chains (such as ETH/BSC/AVAX, etc.) based on the cross-chain interoperability protocol wormhole.
- [DolaProtocol](https://github.com/OmniBTC/DolaProtocol) - A Decentralized Omnichain Liquidity Aggregation Protocol with the single coin pool of each public chain as the core, Wormhole, Layerzero and other cross-chain messaging protocols as the bridge, and Sui public chain as the settlement center.
- [ObjectMarket](https://github.com/coming-chat/object-market) - A unique object trading marketplace in the Sui network.

### SocialFi
- [Dmens](https://github.com/coming-chat/Dmens) - Decentralized Moments which is a Blockchain Twitter Protocol built on the Sui network.

### On-Chain Governance

- [ValidatorUniverse](https://github.com/OLSF/libra/blob/main/language/diem-framework/modules/0L/ValidatorUniverse.move) - Validator set management. Deployed on 0L.
- [Oracle](https://github.com/OLSF/libra/blob/main/language/diem-framework/modules/0L/Oracle.move) - For on-chain community voting. Deployed on 0L.
- [DAO](https://github.com/starcoinorg/starcoin-framework/blob/main/sources/Dao.move) - For on-chain proposals and voting. Deployed on Starcoin.
- [DiemSystem](https://github.com/diem/diem/blob/main/diem-move/diem-framework/DPN/sources/DiemSystem.move) - Validator set management. From Diem.
- [Vote](https://github.com/diem/diem/blob/main/diem-move/diem-framework/experimental/sources/Vote.move) - On-chain voting. From Diem.

### Cross-Chain Bridge

- [Poly Bridge](https://github.com/Elements-Studio/poly-stc-contracts) - The first Cross-Chain Bridge between Move and EVM. Deployed on Starcoin.
- [OmniBTC Bridge](https://github.com/OmniBTC/OmniBridge) - A bridge between Bitcoin and Move language public chains (like Aptos and Sui) based on ultra-light node.

### Accounts

- [Account](https://github.com/diem/diem/blob/main/diem-move/diem-framework/core/sources/Account.move) - A generic account for Diem-powered chains. From Diem.
- [DiemAccount](https://github.com/OLSF/libra/blob/main/language/diem-framework/modules/DiemAccount.move) - Fork of the above. From 0L.
- [Account](https://github.com/starcoinorg/starcoin-framework/blob/main/sources/Account.move) - Fork of the above. From Starcoin.

### Frameworks

A Move **framework** is the set of Move modules included in the genesis state of the chain. 
These modules typically implement key concepts like accounts, currencies, . 
The ability to separate blockchain-specific framework logic from the generic functionality of the Move language is a key part of Move's platform-agnostic design.

- [Sui Framework](https://github.com/MystenLabs/sui/tree/main/crates/sui-framework)
- [Aptos Framework](https://github.com/aptos-labs/aptos-core/tree/main/aptos-move/framework)
- [0L Framework](https://github.com/OLSF/libra/tree/main/language/diem-framework/modules/0L)
- [Starcoin Framework](https://github.com/starcoinorg/starcoin-framework)
- [Diem Framework](https://github.com/diem/diem/tree/main/diem-move/diem-framework/DPN)

### Libraries

- [Move standard library](https://github.com/move-language/move/tree/main/language/move-stdlib) - Utilities intended (but not required) to be used in every platform running Move. From the Move repo.
- [Move nursery](https://github.com/move-language/move/tree/main/language/move-stdlib/nursery) - Experimental modules that may eventually be promoted into the standard library. From the Move repo.
- [Decimal](https://github.com/OLSF/libra/blob/main/language/diem-framework/modules/0L/Decimal.move) - Efficient implementation of a decimal value. From 0L.
- [Math](https://github.com/starcoinorg/starcoin-framework/blob/main/sources/Math.move) - Math utility functions. From Starcoin.
- [Compare](https://github.com/move-language/move/blob/main/language/move-stdlib/nursery/sources/compare.move) - Polymorphic comparison (i.e., compare any two Move values of the same type). From the nursery.
- [Vault](https://github.com/move-language/move/blob/main/language/move-stdlib/nursery/sources/vault.move) - Library for capabilities. From the nursery.
- [ACL](https://github.com/move-language/move/blob/main/language/move-stdlib/nursery/sources/acl.move) - Library for list-based access control. From the nursery.
- [TaoHe](https://github.com/taoheorg/taohe) - A collection of nestable Move resources.
- [Starcoin Framework Commons](https://github.com/starcoinorg/starcoin-framework-commons) - Libraries for Move commons utility on starcoin-framework. From Starcoin.
- [Movemate](https://github.com/pentagonxyz/movemate) - Smart contract building blocks for Aptos and Sui (Math utilities, governance contracts, escrow, and more). Maintained by the Pentagon team.
- [Move cron parser](https://github.com/snowflake-so/move-cron-parser#readme) - Library is built for a purpose of parsing cron expression. Maintained by Snowflake Network team.

### Miscellaneous

- [Move-on-EVM](https://github.com/move-language/move/tree/main/language/evm) - Experimental project to compile Move source code to EVM bytecode.
- [aoc-move](https://github.com/whonore/aoc-move) - Advent of Code solutions in Move with some formal verification.

## Tools

- [Move Package Manager](https://github.com/move-language/move/tree/main/language/tools/move-cli) - Like `cargo` or `npm` for Move: single CLI (and corresponding Rust API's for other tools to hook into) for building, running, testing, debugging, and verifying Move [packages](https://move-language.github.io/move/). Maintained by the Move core team.
- [Move Prover](https://github.com/move-language/move/tree/main/language/move-prover) - Formal verification of user-defined specifications written in Move source code. Maintained by the Move core team.
- [Move Read/Write Set Analyzer](https://github.com/move-language/move/tree/main/language/tools/read-write-set) - Static analysis tool for computing an overapproximation of the global memory touched by a Move program. Maintained by the Move core team.
- [Move Playground JS Library](https://github.com/imcoding-online/js-move-playground) - Wrapping [Move Playground by Pontem](https://playground.pontem.network/) as a JavaScript library for browser. You can use it to build your own Move Playground.
- [go-sui-indexer](https://github.com/coming-chat/go-sui-indexer) - An off-fullnode service to serve data from Sui Node.

## IDEs

- [Move VS Code plugin](https://marketplace.visualstudio.com/items?itemName=move.move-analyzer) - Maintained by the Move core team ([source code](https://github.com/move-language/move/tree/main/language/move-analyzer)).
- [Move IntelliJ plugin](https://plugins.jetbrains.com/plugin/14721-move-language) - Maintained by the Pontem team ([source code](https://github.com/pontem-network/intellij-move)).
- [ChainIDE for Sui](https://chainide.com/) - Sui Move Cloud-Powered Development Platform, maintained by the ChainIDE team.
- [Move Playground](https://playground.pontem.network/) - Like [Remix](https://remix.ethereum.org/) for Move. Alpha version of a Web IDE. See [instructions](https://gist.github.com/borispovod/64b6d23741d8c1f4b0b958a3a74aa68d). Maintained by the Pontem team.
- [Starcoin IDE](https://marketplace.visualstudio.com/items?itemName=starcoinorg.starcoin-ide) - Maintained by the Starcoin team ([source code](https://github.com/starcoinorg/starcoin-ide)).
- [Move Vim](https://github.com/rvmelkonian/move.vim) - Maintained by [@rvmelkonian](https://github.com/rvmelkonian/).
- [move-mode](https://github.com/amnn/move-mode) - Major mode for Emacs maintained by [@amnn](https://github.com/amnn/).

## Package Managers
- [Movey](https://www.movey.net/) - A crates.io-style repository of Move packages.

## Wallets

- [StarMask](https://github.com/starcoinorg/starmask-extension) - A wallet for the Starcoin blockchain. Maintained by the Starcoin team ([Chrome Webstore](https://chrome.google.com/webstore/detail/starmask/mfhbebgoclkghebffdldpobeajmbecfk?hl=en)).
- [Sui Wallet](https://github.com/MystenLabs/sui/tree/main/apps/wallet) - A chrome (v88+) extension wallet for Sui ([Chrome Webstore](https://chrome.google.com/webstore/detail/sui-wallet/opcgpfmipidbgpenhmajoajpbobppdil)).
- [Pontem Wallet](https://github.com/pontem-network/pontem-wallet) - Wallet extension for Aptos network by the Pontem team ([Chrome Webstore](https://chrome.google.com/webstore/detail/pontem-wallet/phkbamefinggmakgklpkljjmgibohnba)).
- [Fewcha Aptos Wallet](https://github.com/fewcha-wallet/fewcha.app) - The wallet of layer 1 blockchain Aptos ([Chrome Webstore](https://chrome.google.com/webstore/detail/fewcha-aptos-wallet/ebfidpplhabeedpnhjnobghokpiioolj)).
- [bcs-js](https://github.com/pontem-network/lcs-js) - JavaScript implementation of the [BCS](https://github.com/diem/bcs) serialization scheme used by Move, may be useful for implementing wallets.
- [ComingChat](https://coming.chat/) - A decentralized social finance/web3 portal.  Supporting public chain wallets, such as Sui and Aptos wallets.
- [Suiet Wallet](https://github.com/suiet/suiet) - A open-source wallet for Sui. ([Chrome Webstore](https://chrome.google.com/webstore/detail/suiet/khpkpbbcccdmmclmpigdgddabeilkdpd), [Website](https://suiet.app)) 
- [Ethos Wallet](https://github.com/EthosWallet/chrome-extension) - Open-source chrome extension wallet for Sui ([Chrome Webstore](https://chrome.google.com/webstore/detail/ethos-sui-wallet/mcbigmjiafegjnnogedioegffbooigli), [Website](https://ethoswallet.xyz/)).

### Wallet Adapters

- [Sui Wallet](https://github.com/MystenLabs/sui/tree/main/sdk/wallet-adapter) - Sui Wallet Adapter.
- [Suiet Wallet](https://github.com/suiet/wallet-adapter) - Suiet Wallet Adapter.

### Wallet Kits

- [Suiet Wallet Kit](https://github.com/suiet/wallet-kit) - A package support all Sui wallets with customizable UI.
- [Ethos Connect](https://github.com/EthosWallet/ethos-connect) - UI with built-in wallet adapter and Email option for supporting all wallets and wallet-less users on Sui.

## SDKs

### Sui SDKs
- [Rust SDK](https://docs.sui.io/devnet/build/rust-sdk) (official)
- [TS/JS SDK](https://github.com/MystenLabs/sui/tree/main/sdk/typescript) (official)
- [Golang SDK 1](https://github.com/coming-chat/go-sui-sdk) (community)
- [Golang SDK 2](https://github.com/block-vision/sui-go-sdk) (community)
- [Python SDK](https://github.com/FrankC01/pysui) (community)
- [Java SDK](https://github.com/GrapeBaBa/sui4j) (community)
- [Kotlin SDK](https://github.com/cosmostation/suikotlin) (community)
- [C# SDK](https://github.com/naami-finance/SuiNet) (community)

### Sui Dapps SDKs
- [OmniSwap-Sui-SDK](https://github.com/OmniBTC/OmniSwap-Sui-SDK) (community)

### Other network SDKs
- [Aptos Golang SDK](https://github.com/coming-chat/go-aptos-sdk) (community)

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

- [The Move Programming Language](https://youtu.be/J1U_0exNFu0)
- [Move on Sui](https://www.youtube.com/watch?v=xMsE1X4wio4)
- [Move on Aptos](https://www.youtube.com/watch?v=gvRJdJTQd8U)
- [Move: A Safe Language for Programming with Money](https://www.youtube.com/watch?v=EG2-7bQNPv4&ab_channel=FieldsInstitute) - Talk from [@sblackshear](https://github.com/sblackshear) at the [Fields Institute Blockchain](http://www.fields.utoronto.ca/activities/seminar_series/blockchain-research-seminar-series) research seminar series.
- [Formal Verification of Move Programs for the Libra Blockchain](http://www.fields.utoronto.ca/talks/Formal-verification-Move-programs-Libra-blockchain) - Talk from [@DavidLDill](https://github.com/DavidLDill) at the [Fields Institute Blockchain](http://www.fields.utoronto.ca/activities/seminar_series/blockchain-research-seminar-series) research seminar series.
- [Move for the Masses](https://www.youtube.com/watch?v=b_2jZ4YEfWc) - Talk at the [Converge '22](https://converge.circle.com/event/4ea0d06f-3900-4b6d-a9cd-aeaedda9ef2e/summary).

## Slides
- [Move deep dive](https://docs.google.com/presentation/d/1Tb2iZD0xrQSlwXIJNL1djNYc0_p0szfB2STgURgHgls/edit?usp=sharing)
- [Move overview](https://docs.google.com/presentation/d/1gU-M42Juz7ARc61unPXphJ_BX1OlQrBwR1VdaPT4M5w/edit?usp=sharing) - Slides from [Reasoning About Financial Systems](https://reasoningaboutfinancialsystems.org/) workshop at [SBC '22](https://cbr.stanford.edu/sbc22/).

## Podcasts

- [Move and Sui with Sam Blackshear from Mysten Labs](https://zeroknowledge.fm/228-2/)
- [Move AMA covering Move origin story](https://twitter.com/i/spaces/1jMKgepNOleJL)

## Blog Posts
- [Comparing Move and Rust smart contract development](https://medium.com/@kklas/smart-contract-development-move-vs-rust-4d8f84754a8f)
- [Comparing Diem-style Move and Sui Move](https://sui.io/resources-move/why-we-created-sui-move)

## Security
- [Aptos-movevm Denial of Service Vulnerability](https://medium.com/numen-cyber-labs/analysis-of-the-first-critical-0-day-vulnerability-of-aptos-move-vm-8c1fd6c2b98e)

## Contributing

Contributions welcome! Read the [contribution guidelines](CONTRIBUTING.md) first.
