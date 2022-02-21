# Problem Statement
We believe web3 development is rapidly outgrowing today's smart contract languages and execution layers. Some key problems we see with today’s solutions are:

1. **Smart contract languages aren’t cross-platform.**
Languages overfit to implementation details of the blockchain they are designed for such as transaction and account structure, signing/hashing algorithms, and consensus algorithm.
This frustrates interoperability, prevents smart contract reuse, and discourages communities from forming across platforms.
A designer of a new platform is faced with a tough choice: either bootstrap an entirely new language and ecosystem, or use an existing language (e.g., Solidity/the EVM) that forces your new platform to inherit many limitations from the old one.
The decentralized web needs a lingua franca that will allow platform creators to experiment with vastly different architectures without needing to create a new language for each one.

2. **Smart contract languages aren't safe enough.**
Multimillion dollar exploits are a [regular](https://rekt.news/) occurrence.
Effective smart contract developers must be experts in both security and their product.
Language design mistakes (e.g., re-entrancy, insufficient access control features, silent integer overflow) increase the attack surface for contracts, make audits expensive and slow, and frustrate the adoption of formal verification.
We believe that insufficient language safety is a serious barrier to both mainstream adoption of digital assets and accessible smart contract development.

3. **Smart contract execution layers aren't fast.**
In most platforms, transaction execution is sequential and low-throughput.
Improving on this is challenging because existing languages are not designed with amenability to parallel execution in mind.
In addition, most languages have unconventional features (e.g., large default integers that don't fit in a register, collections based on collision-resistant hashing with no data locality) that prevent improvements such as effective ahead-of-time or JIT compilation to native code.
Insufficient throughput pushes gas prices to absurd levels and locks out users/use-cases that can’t afford them.

4. **Immature language ecosystems.**
Languages do not provide features for contract composition, leading to [massive code duplication](http://www.ifca.ai/fc20/preproceedings/106.pdf) and wasting expensive on-chain storage.
Conventional languages align on dedicated package managers (e.g., crates.io for Rust, npm for JavaScript pip for Python) for sharing/building code, releases, bug fixes, vulnerability disclosure, etc., but no such package manager exists for smart contract languages.
Instead, developers manually copy/paste and tweak popular templates.
This immaturity makes it difficult to build (and perhaps even more importantly) maintain large applications.

5. **Bad end-user experience.**
End-users are directly exposed to design mistakes in today’s execution layers. 
A basic operation like "view all the assets my account owns" requires scanning the entire blockchain or relying on third-party infrastructure that does so. 
Wallets ask users to sign opaque transactions whose contents (or effects) cannot easily be understood. This opens the door to theft attempts like [poison tokens](https://www.theblockcrypto.com/post/112339/creative-attacker-steals-76000-in-rune-by-giving-out-free-tokens) or [spoofing token approvals](https://www.theverge.com/2022/2/20/22943228/opensea-phishing-hack-smart-contract-bug-stolen-nft).
