# Bitcoin-layer2
Bitcoin Layer 2 Protocols Research
(Lightning network, Liquid network and Rootstock)

##Table of Content

1. Overview of the Layer 2 Protocol
2. Working mechanism or principle
3. Key features, benefits and use cases
4. Strengths, Weaknesses and Challenges
5. Ecosystem and Network Activity
6. Future Outlook
7. Sources

## Overview Of The Bitcoin Layer 2 Protocols
Bitcoin layer-2s aim to scale the network, enhancing programmability in the No. 1 blockchain and unlocking new utilities. With an average block time of 10 mins, a throughput of 7 TPS, and a high transaction cost of 21 USD, as well as Bitcoin’s limited support for smart contracts, Bitcoin layer-2s bring more functionality to the Bitcoin network and, in return, enjoy the security and network effects of Bitcoin.

There are many ways to scale Bitcoin, from sidechains to state channels, rollups, and client-side validation. Each method has its unique approach and technicality. The Lightning Network is arguably the most popular Bitcoin layer 2 and a typical example of state channels, while Liquid Network and Rootstock are examples of sidechains.

## Top Bitcoin Layer 2 protocols

1. Lightning Network,
2. liquid Network 
3. Rootstock

## Lightning Network
Lightning network enables near-instant payments utilising Bitcoin’s native smart contract scripting language. It also allows low fees and reduces transaction confirmation times by processing transactions off-chain, avoiding global consensus and network congestion.

Lightning network utilises payment channels, which are off-chain networks running parallel to the main blockchain, aiming to create a channel between two parties involved in the transaction. Then, the channel interacts with the mainnet at opening or closing, and when the channel is closed down, the latest state is bundled into a single transaction and submitted to the mainnet.


### Working Mechanism Or Principle
Firstly, the Lightning network utilises a network of nodes that transact privately with each other via channels without requiring global consensus. It uses a bidirectional payment channel that involves two users sending and receiving Bitcoins without constantly broadcasting the transactions to the main blockchain.

Suppose two parties, A and B, wish to transact; they open a payment channel by depositing Bitcoin into a 2-of-2 multi-signature (multi-sig) wallet to open an on-chain funding transaction recorded on the mainnet. Similarly, channel closing is also done on-chain.

A and B can now transact off-chain and send funds to each other, and they will both sign every transaction with the channel balance updated each time a transaction is made. Afterwards, both parties can agree to close the transaction, and the funds are sent to their wallets, while the balance represented as a single transaction is broadcast to the Mainnet.

The lightning network also uses Hashed Timelock contracts (HTLC) to conduct secure transfers via many channels and across multiple hops to the final destination, unlike a bidirectional payment, which allows transfers within a channel.

### Key Features, Benefits, And Use Cases

#### Benefits
1. High throughput and fast transactions 
2. Lower fees
3. No third-party trust


#### Use Cases
1. Cross-chain Transactions
Lightning network transactions can be routed over multiple chains with different consensus mechanisms, provided that they enforce similar hash functions across chains. The sender or receiver’s chain doesn't matter.

2. Micropayments
Unlike Bitcoin, lighting network can afford micropayments with cheap transaction fees, for example, payments which are less than a dollar or even a fraction of a cent

#### Key Features
1. Multi-signature addresses
2. Hashed Timelock Contracts (HTLCs)
3. Bidirectional Payment Channels

### Strengths, Weaknesses and Challenges

#### Weaknesses
1. Risk Of Coin Theft
The Lightning Network require nodes and parties to be online to broadcast transactions. The problem is when the nodes go offline, private keys can be compromised and coins stolen. Also, if the transactions are not broadcasted in time or the event of data loss, the second party can steal funds.
The risk of coin theft can be mitigated by using a third party to send funds or having a third-party data storage service. Even if an intermediary node is used, limiting the amount of funds in the hot wallet is crucial.
Coin theft risk also holds sway if invalid time-locked transactions become valid due to insufficient time.  Therefore, participants should select timelocks with ample amount of time.

2. Spam From Forced Expiration
This spam can occur when a bad actor creates many channels and forces them all to expire at once, thereby overwhelming the block data capacity and causing mass spam on the blockchain network, leading to transaction delay until the locked-time transactions are invalid.

#### Challenges
3Privacy is challenging for the lightning network since they rely on a custodial wallet, an aberration to the Bitcoin mantra, “not your key, not your coins. ” Additionally, it is difficult to run a lightning node, so LN relies on a custodial solution, which is easy to set up and use. Another keynote issue with the Lightning network is the difficulty and time-consuming process of finding a well-funded node with a direct channel to the recipient when a user wants to make a payment that exceeds their channel balance.
Other challenges include the costs of opening and closing a channel, which is an on-chain transaction, the risk of a node going offline and being unable to process transactions through the channels it's connected to, as well the risk of double spending, which can occur when a node is offline and hence does not provide the correct transaction state.

### Ecosystem and Network Activity
Bitcoin Brokerage and Services firm River reported about 6.6 million transactions on the Lightning network in August 2023, a 1,212% increase from August 2021 despite a 44% drop in the price of Bitcoin. Gaming, social media tipping, and streaming were the primary use cases driving 27% of the growth. 
River also reported about 279k to 1.116 million monthly active Lightning users as of September 2023. About 179 companies across 28 categories are also participating in the lightning network. At the time of writing, Lightning Network’s TVL is $213.36m, according to Defillama.


### Future outlook
Arguably the most popular Bitcoin layer 2, it scored a significant win when Binance adopted it. Coinbase has also proposed adopting the network. As we march towards global crypto Adoption, the Lighting network will have a pivotal role to play by enhancing Bitcoin’s efficiency and scalability.
The lightning network's future lies in onboarding many merchants and integrating LN into existing payment systems. The LN team is working to achieve this by building partnerships with payment processors and user-friendly point-of-sale systems.


## Liquid Network 
The liquid network is a Bitcoin layer 2 sidechain built on the Bitcoin code base that enables faster transaction finality, privacy and issuance of digital assets on the Bitcoin network. The idea was to enable users to transfer Bitcoin between two networks via a two-way peg. 
The Liquid Network was established in 2015 by Blockstream, which now only serves as the technology provider. 

### Working mechanism or principle
A user sends Bitcoins to a Liquid address (“Peg-in” transaction) to claim an equivalent Liquid Bitcoin (L-BTC) from the Liquid network. The Bitcoin is frozen, and after about 112 confirmations on the Bitcoin network, the L-BTC can be claimed on the Liquid network. The confirmations are security measures intended to protect participants’ funds in the event of Bitcoin chain block reorganisation. Conversely, users can request a Peg-out when they plan to withdraw their BTC. Then, after two liquid confirmations, the Liquid Network releases the BTC to the user’s Bitcoin wallet.
Unlike the Bitcoin network, which utilises the proof–of–work consensus method, the Liquid network is secured by Strong Federation, essentially a group of non-trusting participants called functionaries responsible for signing blocks and securing the Bitcoin held by the network.
Although anyone can run a node and verify the network state, the Liquid network is operated by members consisting of financial firms, Bitcoin companies, and big exchanges distributed globally.

### Key features, benefits and use cases

#### Benefits
1. Instant Settlement
2. Privacy and confidentiality
Liquid Network users enjoy confidentiality when making transactions; this is ensured by using cryptography to hide transaction details like the amount and asset type being transferred from everyone except for the sender and receiver.
3. Multiple Assets and Tokenization
Users can issue, buy and sell security and utility tokens and stablecoins on the Liquid Network.

#### Use cases
Typical use cases for the Liquid Network include the creation of security tokens using Liquid’s Issued Assets feature and the issuance of stablecoins and tokenised cryptocurrencies. Other use cases include faster fund transfer and helping to capitalise on trading opportunities quickly.

#### Key features 
1. Swaps 
In the liquid network, swaps are single, trustless transactions that complete the exchange of assets between two parties without one party trusting the second party to complete his part of the transaction. Swaps are usually completed using the Partially Signed Elements Transaction (PSET) standard.

### Strengths, Weakness And Challenges

#### Weakness
1. Risk Of Censorship And Malicious Attack 
The presence of only pre-selected functionaries to validate and generate blocks raises censorship concerns and the risk of malicious attacks, unlike the Bitcoin network, which runs over 13,000 nodes and is almost impossible to shut down.

### Ecosystem And Network Activity

### Future Outlook
The Liquid Network provides solutions for financial institutions and has attracted significant players like Binance, Blockstream and BitFinex. Hopefully, this focus on established institutions will translate to further adoption.



## Rootstock 
Rootstock is a sidechain built on the Bitcoin codebase that allows developers to bring smart contract functionality and integrate DeFi dApps into the Bitcoin ecosystem.
Through its merged mining feature, Roostock shares the security and robustness of the Bitcoin network. Merged mining involves miners mining for Roostock and Bitcoin simultaneously without additional resources.
Beyond Bitcoin, Rootstock is EVM compatible and allows the deployment of Ethereum smart contracts and bridging assets between Roostock and Ethereum Networks.

### Working Mechanism Or Principle
Rootstock works similarly to other Bitcoin sidechains. For a transaction to occur, Bitcoin is transferred to the Rootstock network (SmartBitcoins, SBTC). SBTC is equivalent in value to Bitcoin and can be transferred back to the Bitcoin Network, incurring only the RSK transaction fee denominated in RBTC, used to pay miners who process the transactions.

### Key Features, Benefits And Use Cases

#### Benefits
1. Fast Transaction Confirmation Times 
Rootstock averages a block confirmation time of 30 seconds, which can be lowered by miners and can support about ten transactions per second.
2. Opportunities For Miners
With every halving, the mining rewards continue to drop, and so does the profitability of the mining business. Rootstock provides an alternative for miners who have invested in mining hardware to diversify through its merged mining and extend the lifespan of their business, as they can utilise their resources to mine both Rootstock and Bitcoin with zero marginal costs.
3. Lower Transaction Fees
As a sidechain, Rootstock significantly reduces the cost of transacting directly on the Bitcoin Network.
4. EVM Compatibility
Developers can transfer existing EVM dApps and build new ones on a Rootstock using familiar coding language.

#### Use Cases
Rootstock's applications span different needs and industries, from micropayments and micro-lending to everyday retail payments, creation and issuance of digital assets, asset tokenisation, supply-chain, digital identities and more.

#### Key Features 
1. A two-way pegged protocol (Powpeg)
RBTC is two-way pegged to the BTC and can be exchanged freely 1:1 without price negotiation. It is the duty of the STTP (Semi Trusted Third Parties), which are members of the Federation, to protect and unlock the locked BTC.

2. Merged Mining
Merged Mining involves miners mining for Roostock and Bitcoin simultaneously with the same resources. This is possible since both use the proof-of-work method of consensus.

### Strengths, Weakness and Challenges

#### Weaknesses

#### Challenges
1. Competition
Rootstock faces significant competition with other Bitcoin scaling solutions like the Lightning Network, which delivers a superior throughput of about a million transactions per second compared to Rootstock’s 300 TPS.
 2. Limited Adoption
However awesome the tech, the global adoption of Bitcoin layer 2s in infant stages and may take considerable time before they become m.ainstream
3. Security Risk
Two-way pegged Bitcoin sidechains like Rootstock may require additional protection due to double-spend and other vulnerabilities and could be a target for hackers.

### Ecosystem And Network Activity
Rootstock has about $114.07m in TVL at the time of writing, according to Defillama, showing substantial investor interest. The network also boasts over 140 dApps, about 68,400 monthly transactions, 47 protocols on the network and an active developer community. Several projects, including exchanges and DeFi trading platforms like UniSwap, Oku, and AirSwap, have integrated Rootstock, not to mention leading wallet providers Ledger and Exodus.

### Future outlook
EVM-compatible protocol, Rootstock combines the benefits of Bitcoin and Ethereum and will give developers better options when building dApps. As the use cases of Bitcoin expand beyond value transfers, the demand for faster transactions and smart contract functionality will increase, and Rootstock will position itself as a solution for a wide range of applications.


## Sources
https://lightning.network/lightning-network-paper.pdf

https://cointelegraph.com/news/the-state-of-the-bitcoin-lightning-network-in-2023
https://river.com/learn/files/river-lightning-report-2023.pdf
https://beincrypto.com/bitcoin-lightning-network-transactions-research/
https://cointelegraph.com/news/binance-integration-bitcoin-btc-lightning-network

https://hackernoon.com/a-beginners-guide-to-the-liquid-network
https://docs.liquid.net/docs/technical-overview
https://liquid.net/


https://blog.rootstock.io/wp-content/uploads/2019/02/RSK_White_Paper-ORIGINAL.pdf
https://blog.rootstock.io/noticia/rsk-executive-overview-february-2022/

https://rskgasstation.info/?AspxAutoDetectCookieSupport=1
https://twitter.com/rootstock_io/status/1740805633069228405
https://hackernoon.com/defi-on-bitcoin-part-1-a-guide-to-building-dapps-with-rootstock
https://crypto.com/university/what-are-bitcoin-layer-2s
https://blog.rootstock.io/noticia/rootstock-vs-ethereum-why-more-developers-are-choosing-to-build-on-rootstock/
https://dev.rootstock.io/rsk/architecture/mining/
https://blog.rootstock.io/noticia/syncchain-synchronized-sidechains-for-improved-security-and-usability/
