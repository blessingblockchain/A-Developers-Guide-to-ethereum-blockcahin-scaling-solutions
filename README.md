# A-Developers-Guide-to-ethereum-blockcahin-scaling-solutions

Ethereum's emphasis on decentralization and security means that transactions are processed slowly. This affects network throughput and impacts the ability of decentralized applications (dApps) to scale. 

Many designs have been proposed to solve Ethereum's scalability problems, each offering different benefits. This guide will introduce Ethereum scaling solutions and explain how they work and why they matter. 

What is scalability?
Scalability refers to the ability of a system to handle exponential increases in usage without sacrificing functionality. In the context of blockchain technology, scalability means a blockchain's capacity to support increased transactions without any effects on functionality. 

Currently, Ethereum's ability to handle transactions is limited to processing 7-15 transactions per second (TPS). Conversely, traditional, centralized databases—like Oracle Database and Microsoft SQL Server—can process thousands of transactions per second.


Source: Blockchair
Two Ways Ethereum’s Design Affects Scalability
Ethereum has low throughput and slow processing speeds because it prioritizes decentralization and security ahead of scalability (scalability trilemma). 

Here are some ways Ethereum's design affects scalability:

1. Ethereum’s consensus algorithm processes transactions sequentially
Ethereum uses proof of work (PoW), which means transactions on the network must be accepted and validated by all nodes. This encourages decentralization and, more importantly, security. 

The downside is that the sequential execution of transactions affects transaction finality (the time it takes to confirm a transaction). This further contributes to Ethereum's inability to support high TPS rates. 

2. Ethereum limits block sizes to 1MB
Ethereum limits how much data a mined block can hold (1MB) because capping the block size improves decentralization by enabling nodes to more effectively store the blockchain history. Bigger block sizes make it difficult for people to run full nodes, harming decentralization. 

However, the block size limit of 1MB reduces the transaction data miners can fit into one block, affecting network throughput. Small block sizes also affect the cost of gas, the computational resource required to execute operations in the Ethereum Virtual Machine. 

Because miners have finite computational power, they are often forced to prioritize transactions with higher fees. This creates a bidding war of sorts between Ethereum users and forces astronomical increases in transaction fees. 

What are Ethereum scaling solutions?
Ethereum scaling solutions are platforms specifically designed to improve transaction execution on the Ethereum network. Ethereum scaling solutions like layer 2 rollups and sidechains are protocols that use different mechanisms to increase network throughput. 


Source: Reddit
Layer 1 vs Layer 2 Scaling Solutions
Scaling solutions can be broadly divided into two categories, "on-chain," and "off-chain," solutions that are differentiated based on their point of execution. 

Layer 1 scaling solutions
Layer 1 scaling involves making changes to the blockchain network and rewriting the base layer. The "on-chain" description means scaling upgrades to Ethereum are executed on the blockchain itself. 

Layer 1s can scale by increasing block sizes 
A potential Layer 1 scaling improvement is increasing the block size. If Ethereum's 1MB block size increased, miners would have more space to include additional transaction data in blocks. 

While increasing Ethereum’s block size would lead to an increase in TPS rates, the side effect is a slow progression towards centralization because as block sizes grow, the blockchain's size increases—making it difficult to run a full node (except if you have a supercomputer). For this reason, the Ethereum community has ruled out bigger block sizes as a scaling solution. 

Layer 1s can scale by processing transactions in parallel with blockchain sharding 
Blockchain sharding is a scalability improvement that introduces parallel execution of transactions in place of the default sequential execution model Ethereum uses. In sharding, the blockchain is divided into smaller chains (shards) that validate and process separate transactions. 

Consider how Ethereum currently works:

Transactions are broadcasted throughout the network until they can be validated. Sharding doesn't require transactions to be approved by all nodes. Instead, each shard has validators (called collators) for approving transactions. 

Each collation (a collection of transactions on the shard chains) must be signed by ⅔ of collators. Also, the proposed collation must be added to the main chain before achieving finality. Together, these measures help assure the security of the system. 

With sharding, Ethereum can increase TPS without sacrificing decentralization or security. As shard chains process different transactions concurrently, the network's overall processing capacity increases. Moreover, network participants can still prove the validity of shard collations through cryptographic proofs.


Source: Genesis Block
Layer 2 scaling solutions
Layer 2 (L2) scaling improvements are so-called because they are executed off the main chain (Layer 1). Also called "off-chain" solutions, Layer 2 scaling involves processing transactions on a separate network that relies on the main chain for security. 

L2 solutions are often designed with an emphasis on transaction speed and scalability—decentralization and security are lesser concerns here. Because they post transaction data to the main Ethereum layer, L2s can benefit from the mainnet's decentralization and security. Also because L2 solutions are built on top of Ethereum, they don’t need their own native token.   

These off-chain protocols can aggregate multiple transactions into a single transaction and add to the main chain. This reduces pressure on the network and improves the potential of dApps to scale as usage grows. 

Examples of Layer 2 scaling solutions include:

Rollups
State channels 
Plasma 
Validium 
Layer 2 vs. Sidechains
A sidechain is a separate blockchain that interacts with Ethereum Mainnet but doesn't rely on it for security. Sidechains connect with Ethereum via a cross-chain bridge, which enables asset transfers between the two chains. 

Sidechains are good for scalability because they are engineered with a different set of qualities that enables high throughput. For instance, the Polygon sidechain uses a proof of stake (PoS) consensus algorithm for faster transactions. 

The main difference between Layer 2 solutions and sidechains lies in their security guarantees. While L2 networks enjoy Ethereum's security assurances, sidechains do not. 

A sidechain is secured by its consensus mechanism, while L2s benefit from Ethereum's consensus. This is why many consider L2s more secure than sidechains. 

Why are scaling solutions necessary for Ethereum?
Good Ethereum scaling solutions help provide web3 developers and users with lower gas fees and faster transactions, while also keeping transactions secure. 

Here's why scaling solutions are necessary for Ethereum:

1. Lower transaction fees 
Ethereum's gas fee problem has become fodder for widespread criticism. Scaling improvements can reduce network congestion and lead to significant drops in transaction costs. 

Lower gas prices translate into a better user experience and higher adoption for dApps. Users won't have to deal with failed transactions or pay exorbitant gas fees.

2. Faster transactions 
Many scaling solutions were created specifically to improve Ethereum's ability to handle more transactions in a shorter time frame. 

For example, rollups can batch thousands of off-chain transactions into a single on-chain transaction. Similarly, sharding increases throughout by encouraging parallel processing of transactions. 

The net result of these improvements is an increase in transactions per second (TPS) rates. Although estimates vary, many expect L2s and sharding to push Ethereum's TPS into the thousands. 

3. Improved Security 
L2s are great for scaling Ethereum without decreasing network security. Unlike on-chain scaling, off-chain scaling projects don't affect Ethereum's decentralization.  

Even though these L2s are separate chains, their security is tightly linked to the Ethereum blockchain. This means users can safely interact with these projects, enjoying the benefits of scalability, without risking their assets. 

The Five Most Popular Ethereum Scaling Solutions
The five most popular Ethereum Scaling solutions are: rollups, sidechains, state channels, plasma chains, and Validium.

1. Rollups
Rollups combine or "roll up" multiple transactions executed off-chain into a batch and pass it onto the main chain. A single rollup can contain hundreds, if not thousands, of transactions compressed to reduce transaction volumes the main chain has to process. 

Beyond improving scalability, rollups offer levels of security similar to Ethereum itself because transactions in rollups are anchored to the L1 chain, which guarantees transaction finality. 

There are two main types of rollups: optimistic rollups and zero-knowledge rollups. Each type differs based on how transactions are computed and posted to Ethereum:

Zero-knowledge rollups or ZK-rollups perform computation off-chain and generate a cryptographic proof called a Succinct Non-Interactive Argument of Knowledge (SNARK) or Succinct Transparent Argument of Knowledge (STARK). These "validity proofs" assures nodes on the main chain of the validity of transaction batches. 

Optimistic rollups assume transactions are valid by default and don't generate validity proofs for every transaction bundle. However, the validity of transactions in optimistic rollup can be challenged via a fraud proof. 

So how do both rollup schemes stack up against each other? ZK-rollups are more secure since they generate validity proofs, however, this makes them slower than optimistic rollups. 

ZK-rollups are complex mechanisms, which makes it hard to program EVM compatibility into them. As a result, ZK-rollups have limited functionality compared to optimistic rollups. 

Polygon is working on a zero-knowledge EVM (zkEVM) to increase the functionality of zero-knowledge rollups to the Ethereum network with their plans for Hermez 2.0.

Ethereum L2s using Optimistic Rollups
Optimism 
Arbitrum 
Boba Network 
Immutable X 
Ethereum L2s using ZK Rollups
zkSYNC
Loopring 
dYdX
StarkNet 
As a developer, you can integrate rollups into your dApp to improve transaction finality and scalability. This way, your users don't have to experience high gas fees, dropped transactions, and slow processing speeds—which happen frequently on Ethereum. 

2. Sidechains 
A sidechain is one type of layer 2 solution that is a separate blockchain which operates in parallel with the Ethereum Mainnet. These differences could be cryptoeconomic incentives, consensus mechanisms, and so on. 

Sidechains designed specifically for Ethereum have Ethereum Virtual Machine (EVM) compatibility and can support smart contracts. This means you can deploy projects on sidechains and leverage their scalability improvements for dApps. 

Cross-chain bridges are necessary for connecting sidechains to the Ethereum smart contract platform. Just like the name suggests, a blockchain bridge provides a gateway for users to move between the main chain and sidechain.  

To use a bridge you have to lock up some assets (ETH in this case) on the origin chain. Afterward, an equal amount of assets are produced on the sidechain and deposited in your wallet. 

You can then transact freely on the sidechain, taking advantage of its superior transaction processing capabilities. As explained earlier, sidechains are engineered to provide scalability and employ different mechanisms to achieve that. 

Ethereum Sidechain Examples:
Polygon
xDAI 
SKALE
Other alternative Layer 1 (L1) blockchains can also function as Ethereum sidechains, especially the EVM-compatible blockchains. These alt L1s often offer benefits like lower gas fees, better transaction finality, and richer functionality in certain cases. 

Examples of EVM-compatible L1s:
Avalanche
Fantom 
Binance Smart Chain 
3. State Channels 
State channels are off-chain scaling solutions that allow two parties to transact without the main chain having to validate every transaction. A state channel is essentially a multi-signature smart contract that executes only with the approval of the required parties.

How State Channels Work
1. Alice wants to open a state channel with Bob, who sells her coffee every morning. Let's assume she deposits 0.4 ETH in the channel and this transaction is published on Mainnet. 

2. After this opening transaction, Alice and Bob can execute transactions off-chain for as long as they want. The only caveat is that both must sign transactions, which means Alice and Bob must approve each payment for coffee. 

3. If Alice exhausts her deposit, she can publish an exit transaction on the main chain. This transaction will reflect the last known state of the channel, which is then recorded for finality. Alice and Bob may have transacted on a dozen occasions, but the Ethereum network records only two transactions—the entry and exit transactions. 

A state channel allows parties to conduct secure off-chain transactions without having to experience long waiting times and high transaction fees. It also improves scalability because miners have fewer transactions to process and can work faster. 

Ethereum Scaling Solutions That Use State Channels:
Raiden Network
Connext Network
Celer Network
4. Plasma Chains
The Plasma whitepaper introduces the concept of “child chains”, which originate from the main blockchain or “root chain.” While Plasma chains can validate transactions, they rely on the security of the root chain. To prove the validity of transactions, child chains submit cryptographic proofs to the root chain. 

Plasma chains are similar to sidechains, as they connect with the Ethereum blockchain via smart contracts. Using a Plasma chain requires locking up ETH in a smart contract on the root chain before getting tokens on the child chain. 

Plasma is considered an L2 scaling solution because it derives security directly from Ethereum's base layer. This is what makes them safer than, say, sidechains. 

Plasma publishes Merkle roots for each block on the Ethereum main chain. Block roots are small pieces of information we can use to verify information about transactions. If an attack happens on a Plasma chain, users can safely exit to the main chain and withdraw their funds using the appropriate proofs. 

Ethereum Scaling Solutions Using Plasma
OMG Plasma 
Gluon Network
5. Validium 
Validiums are similar to ZK-rollups, performing computation off the main Ethereum layer, but major difference is that validiums use "off-chain data availability" instead of posting compressed data on the main chain like ZK-rollups. 

Validiums store data off-chain with a data provider, making them custodial to some extent. However, some solutions like StarkWare use Data Availability Committees (DACs) to ensure data providers behave honestly. 

Validiums have very low fees and speedy transactions (up to 100,000 tps). However, they have more trust assumptions than other scaling solutions, like ZK-rollups. 

ETH Scaling Solutions Using Validium:
DiversiFi 
Immutable X 
# What are some downsides to scaling solutions?
Two downsides to Ethereum scaling solutions include they’re complex to implement and potentially have lower security guarantees.

1. Complexity 
Many scaling solutions are complex to implement, which can affect their functionality. For instance, the Ethereum development team has consistently pushed back the release date for sharding due to the amount of work the upgrade needs. 

2. Lower security guarantees 
While many L2 and L1 scaling solutions rely on Ethereum for security, they cannot be as secure as the former. Each scaling solution trades off some elements (like decentralization and security) for speed. Users must be well aware of these risks before using these platforms.  

# Conclusion
Scaling projects covered in this guide will likely play a big role in Ethereum's drive towards scalability. Whether this will be enough to guarantee long-term scale remains to be seen, though.  

