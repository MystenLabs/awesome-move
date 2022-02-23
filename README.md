# awesome-move
Code and content from the [Move](https://github.com/diem/move) programming language community.

Move is a programming language for writing safe smart contracts originally developed at Facebook to power the Diem blockchain. Move is designed to be a platform-agnostic language to enable common libraries, tooling, and developer communities across diverse blockchains with vastly different data and execution models. Move's ambition is to become the "JavaScript of web3" in terms of ubiquity--when developers want to quickly write safe code involving assets, it should be written in Move.

# Overview
* [Installation](https://github.com/diem/move/tree/main/language/tools/move-cli#installation)
* [Problem Statement](docs/problem_statement.md)

# Move-Powered Blockchains
* [0L](https://github.com/OLSF/libra) (in [mainnet](https://0l.network/))
* [StarCoin](https://github.com/starcoinorg/starcoin) (in [mainnet](https://stcscan.io/))
* [Pontem](https://github.com/pontem-network) (in [testnet](https://polkadot.js.org/apps/?rpc=wss://testnet.pontem.network/ws#/explorer))
* [Celo](https://github.com/celo-org) ([coming soon](https://www.businesswire.com/news/home/20210921006104/en/Celo-Sets-Sights-On-Becoming-Fastest-EVM-Chain-Through-Collaboration-With-Mysten-Labs))
* [Diem](https://github.com/diem/diem)

# Books
* https://diem.github.io/move/. Maintained by the Move core team.
* https://move-book.com/. Maintained by [@damirka](https://github.com/damirka).

# Tutorials
* [Implementing, testing, and verifying a fungible token](https://github.com/diem/move/tree/main/language/documentation/tutorial). Maintained by the Move core team.

# Community
* [Move Language Discord](https://discord.gg/kRDkxyEt)
* [Move @ Mysten Labs](https://discord.gg/yyYQcckG)
* [Move @ 0L](https://discord.com/invite/Ry2cf4NrbS)
* [Move @ StarCoin](https://discord.gg/Sek9Cnxt)

# Code

## Fungible Tokens
* [BasicCoin](https://github.com/diem/move/tree/main/language/documentation/examples/experimental/basic-coin): a toy implementation of an [ERC20](https://ethereum.org/en/developers/docs/standards/tokens/erc-20/)-like fungible token.
* [Diem](https://github.com/OLSF/libra/blob/main/language/diem-framework/modules/Diem.move): an ERC20-like token with permissioned minting/burning, see also this [spec](https://github.com/diem/dip/blob/main/dips/dip-20.md). Deployed on 0L.
* [Token](https://github.com/starcoinorg/starcoin/blob/master/vm/stdlib/sources/Token.move): another ERC20-like Token. Deployed on StarCoin.
* [GAS](https://github.com/OLSF/libra/blob/main/language/diem-framework/modules/0L/GAS.move): a token that instantiates the Diem standard above. Deployed on 0L.
* [STC](https://github.com/starcoinorg/starcoin/blob/master/vm/stdlib/sources/STC.move): a token that instantiates the StarCoin standard above. Deployed on StarCoin.
* [WEN stablecoin](https://github.com/wenwenprotocol/wen-protocol). Deployed on StarCoin.
* [FAI stablecoin](https://github.com/BFlyFinance/FAI). Deployed on StarCoin.
* [FLY stablecoin](https://github.com/BFlyFinance/FLY): a fork of [Ohm](https://www.olympusdao.finance/) implemented in Move. Deployed on StarCoin.
* [Synthetic token backed by a basket containing a reserve of other tokens](https://github.com/OLSF/libra/blob/main/language/diem-framework/modules/XDX.move). From Diem.

### Non-Fungible Tokens
* [NFT](https://github.com/starcoinorg/starcoin/blob/master/vm/stdlib/sources/NFT.move): an ERC721-like token. Deployed on StarCoin.
* [Merkle Airdrop](https://github.com/starcoinorg/starcoin/blob/master/vm/stdlib/sources/MerkleNFT.move): utility for airdropping a large number of NFT's. Deployed on StarCoin.
* [NFT](https://github.com/diem/diem/blob/main/diem-move/diem-framework/experimental/sources/NFT.move): an implementation of a hybrid ERC721/ERC1155-like token. From Diem.
* [BARS](https://github.com/diem/diem/blob/main/diem-move/diem-framework/experimental/sources/BARS.move): an NFT that instantiates this hybrid standard. From Diem.
* [MultiToken](https://github.com/starcoinorg/starcoin/tree/master/vm/stdlib): an ERC1155-like token. From Diem.
* [NFTGallery](https://github.com/diem/diem/blob/main/diem-move/diem-framework/experimental/sources/NFTGallery.move): utility for holding multiple NFT's of the same type. From Diem.

### DeFi
* [CoinSwap](https://github.com/diem/move/tree/main/language/documentation/examples/experimental/coin-swap) a toy implementation of a [Uniswap](https://uniswap.org/)-like liquidity pool containing two tokens.
* [StarSwap](https://github.com/Elements-Studio/starswap-core): a Uniswap-style DEX. Deployed on StarCoin.
* [Offer](https://github.com/diem/move/blob/main/language/move-stdlib/nursery/sources/Offer.move): generic implementation of atomic swaps for any pair of assets. 

### On-Chain Governance
* [ValidatorUniverse](https://github.com/OLSF/libra/blob/main/language/diem-framework/modules/0L/ValidatorUniverse.move): validator set management. Deployed on 0L.
* [Oracle](https://github.com/OLSF/libra/blob/main/language/diem-framework/modules/0L/Oracle.move) for on-chain community voting. Deployed on 0L.
* [DAO](https://github.com/starcoinorg/starcoin/blob/master/vm/stdlib/sources/Dao.move) for on-chain proposals and voting. Deployed on StarCoin.
* [DiemSystem](https://github.com/diem/diem/blob/main/diem-move/diem-framework/DPN/sources/DiemSystem.move): validator set management. From Diem.
* [Vote](https://github.com/diem/diem/blob/main/diem-move/diem-framework/experimental/sources/Vote.move): on-chain voting. From Diem.

### Accounts
* [Account](https://github.com/diem/diem/blob/main/diem-move/diem-framework/core/sources/Account.move): a generic account for Diem-powered chains. From Diem.
* [DiemAccount](https://github.com/OLSF/libra/blob/main/language/diem-framework/modules/DiemAccount.move): fork of the above. From 0L.
* [Account](https://github.com/starcoinorg/starcoin/blob/master/vm/stdlib/sources/Account.move): fork of the above. From StarCoin.

### Frameworks

A Move **framework** is the set of Move modules included in the genesis state of the chain. 
These modules typically implement key concepts like accounts, currencies, . 
The ability to separate blockchain-specific framework logic from the generic functionality of the Move language is a key part of Move's platform-agnostic design.

* [Diem Framework](https://github.com/diem/diem/tree/main/diem-move/diem-framework/DPN)
* [0L Framework](https://github.com/OLSF/libra/tree/main/language/diem-framework/modules/0L)
* [StarCoin Framework](https://github.com/starcoinorg/starcoin/tree/master/vm/stdlib)

### Libraries
* [Move standard library](https://github.com/diem/move/tree/main/language/move-stdlib): utilities intended (but not required) to be used in every platform running Move. From the Move repo.
* [Move nursery](https://github.com/diem/move/tree/main/language/move-stdlib/nursery): experimental modules that may eventually be promoted into the standard library. From the Move repo.
* [Decimal](https://github.com/OLSF/libra/blob/main/language/diem-framework/modules/0L/Decimal.move): efficient implementation of a decimal value. From 0L.
* [Math](https://github.com/starcoinorg/starcoin/blob/master/vm/stdlib/sources/Math.move): math utility functions. From StarCoin.
* [Compare](https://github.com/diem/move/blob/main/language/move-stdlib/nursery/sources/Compare.move): polymorphic comparison (i.e., compare any two Move values of the same type). From the nursery.
* [Vault](https://github.com/diem/move/blob/main/language/move-stdlib/nursery/sources/Vault.move) and [ACL](https://github.com/diem/move/blob/main/language/move-stdlib/nursery/sources/ACL.move): libraries for capability and list-based acess control. From the nursery.
* [TaoHe](https://github.com/taoheorg/taohe): a collection of nestable Move resources.

### Miscellaneous
* [Experimental](https://github.com/diem/move/tree/main/language/evm/examples) project to compile Move source code to EVM bytecode.

# Tools
* [Move Package Manager](https://github.com/diem/move/tree/main/language/tools/move-cli). Like `cargo` or `npm` for Move: single CLI (and corresponding Rust API's for other tools to hook into) for building, running, testing, debugging, and verifying Move [packages](https://diem.github.io/move/packages.html). Maintained by the Move core team.
* [Move Prover](https://github.com/diem/move/tree/main/language/move-prover). Formal verification of user-defined specifications written in Move source code. Maintained by the Move core team.
* [Move Read/Write Set Analyzer](https://github.com/diem/move/tree/main/language/tools/read-write-set). Static analysis tool for computing an overapproximation of the global memory touched by a Move program. Maintained by the Move core team.

# IDE's
* Move vscode plugin ([install](https://marketplace.visualstudio.com/items?itemName=move.move-analyzer), [source code](https://github.com/diem/move/tree/main/language/move-analyzer)). Maintained by the Move core team.
* Move IntelliJ plugin ([install](https://plugins.jetbrains.com/plugin/14721-move-language), [source code](https://github.com/pontem-network/intellij-move))
* [Move Playground](https://playground.pontem.network/), [instructions](https://gist.github.com/borispovod/64b6d23741d8c1f4b0b958a3a74aa68d). Like [Remix](https://remix.ethereum.org/) for Move--alpha version of a Web IDE. Maintained by the Pontem team.

# Wallets
* StarMask ([install](https://chrome.google.com/webstore/detail/starmask/mfhbebgoclkghebffdldpobeajmbecfk?hl=en), [source code](https://github.com/starcoinorg/starmask-extension)). A wallet for the StarCoin blockchain. Maintained by the StarCoin team.
* [bcs-js](https://github.com/pontem-network/lcs-js). JavaScript implementation of the [BCS](https://github.com/diem/bcs) serialization scheme used by Move, may be useful for implementing wallets.

# Papers

### Language Design
* [Move: A Language With Programmable Resources](https://developers.diem.com/papers/diem-move-a-language-with-programmable-resources/2019-06-18.pdf). This was the original Move white paper released in 2018. Many aspects of this are now out of date (e.g., the syntax and description of the bytecode instructions), but the first two sections are worth a read for explaining the difficulties of programming with assets and how Move tackles them.
* [Robust Safety for Move](https://arxiv.org/abs/2110.05043)
* [Resources: A Safe Language Abstraction for Money](https://arxiv.org/abs/2004.05106)

### Static Analysis and Verification
* [Fast and Reliable Formal Verification of Smart Contracts with the Move Prover](https://arxiv.org/abs/2110.08362)
* [The Move Prover](https://research.facebook.com/publications/the-move-prover/)
* [Verification of Programs Written in Libra's Move Language](https://ethz.ch/content/dam/ethz/special-interest/infk/chair-program-method/pm/documents/Education/Theses/Constantin_M%C3%BCller_MS_Report.pdf)
* [Exact and Linear-Time Gas-Cost Analysis](https://research.facebook.com/publications/exact-and-linear-time-gas-cost-analysis/)

# Videos
* [Move: A Safe Language for Programming with Money](https://www.youtube.com/watch?v=EG2-7bQNPv4&ab_channel=FieldsInstitute). Talk from [@sblackshear](https://github.com/sblackshear) at the [Fields Institute Blockchain](http://www.fields.utoronto.ca/activities/seminar_series/blockchain-research-seminar-series) research seminar series.
* [Formal Verification of Move Programs for the Libra Blockchain](http://www.fields.utoronto.ca/talks/Formal-verification-Move-programs-Libra-blockchain). Talk from [@DavidLDill](https://github.com/DavidLDill) at the [Fields Institute Blockchain](http://www.fields.utoronto.ca/activities/seminar_series/blockchain-research-seminar-series) research seminar series.
