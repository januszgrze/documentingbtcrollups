Disclaimer: I am learning about these technologies and really don't have any knowledge on them. If anything in the notes is glaringly incorrect, please let me know. This repository is a learning excercise for myself, but I'm sharing in case it is valuable for others as well.

[Spaces link](https://twitter.com/lightcoin/status/1633167389675143170)

## Key points

### Intro

"Sovereign rollups just like rollups on ethereum, but they expect users to adjudicate finality for themselves, instead of outsourcing that to the L1 which means you have lower fees, but you can also run rollups on chains that don’t have native smart contract support"

#### Why now?

The invention of non-sovereign rollups as L2s on ethereum, and giving people the opportunity to see how these things work in real tie

Taproot, which gives Bitcoin much more witness space (390,000 bytes of data or if you work with a miner out of band you can get up to 4mb of data). This opens up the design space for the types of protocols you can build on Bitcoin.

New advances in zero knowledge technology gives Bitcoin the opportunity to build trust minimized bridges that give Bitcoin real layer 2s.

Main consensus chain is that there is a need for a cryptographic proof, verification opcode, if you want validity rollups for fully validating bridges

- Optimistic proof can use generalized convenance

Additional policy changes are needed, increasing the amount of data that could be operated on within a script. Increase that limit, give full nodes the ability to validate these validity proofs, then you could have scripts on the l1 that are rollup smart contracts, full nodes or trustless light clients that can fully validate the movement of funds between the l1 and the rollup.
Opcode validity proofs

#### Ultra light client

ZKP system in core software but not in bitcoin core script

- Basically allows you to validate blocks by checking zkp of someone who validated blocks so you don’t have to validate all blocks yourself

Zero sync is doing this

- Develops succinct proof that allows you to check all of bitcoin history in a few seconds. New full nodes can sync node instantly

Why zkp verifier opcode?

- Sovereign rollups allow you to interact trustlessly in the side chain, but not between main chain and side chain. You need a trust minimized bridge to run transactions like inserting X bitcoin for NFT in return

#### Why sovereign vs smart contract rollup

You want sovereign rollups for chains who don’t not have native smart contracts

You can run riskier opt-in experiments on top of the main chain without applying the risk to said main chain

Lower cost because all data is verified off chain which is less burden on the full nodes when compared to ZKP verifiers

Sovereign rollups is different because its the end user who decides what tx’s have happened, account balances, and it gives users ability to fork the rollups. Ethereum, for example, has enshrined smart contract which has final say over everything i.e. your account balance.

In practice we’re not sure if this happens but it gives the users the ability to hard fork as there is no trust minimized bridges. You don’t need permission from third party change

#### Will sovereign rollups get meaningful adoption

Certainly possible. You can look at current side chain models to see how things might play out. But, with sovereign rollups you get full double spend security from bitcoin, and data availability, which could be important for certain use cases. I.e. rollups on top of your sovereign rollup would require more data availability.

Another exciting use case is for developers who want to build l2s on Bitcoin, they can get a head start and understand what that would feel like (before Bitcoin makes opcode changes to enable trustless/trust-minimized bridges) by developing sovereign rollups. You can start with a sovereign rollup and then graduate to an l2 rollup once those capabilities are there.

Another example, Liquid federations could confiscate a token you hold because they’re compromised. With sovereign rollups this isn’t the case because while you’re taking on code risk, you’re not taking on trust assumptions from a third party (there was push back on this. You could potentially preserve assets in some situations if you can gather social consensus from the community at large)

Something cool about NFTs on Bitcoin is that they’re on the main chain. With sovereign rollups, this is the case because the NFT data on the rollup is still stored on a Bitcoin block. But you can also get a new realm of capabilities, like NFT capabilities on Ethereum, that can be enabled, in a trustless way, by the rules enforced by your full node. (I struggled with this, but seems that you can do some cool Ethereum-like stuff).

### Q&A

What are the trust assumptions with using off chain data availability?

- You could run a script or a smart contract on the main chain that validates that Celestia block headers were validated ⅔ of Celestia (for example) validators. Your off chain data availability is relying on a committee based assumption (relying on them to be honest). This example could be possible if Bitcoin adds zkp verification opcode.

Are there any tokens involved on sovereign rollups?

- Depends on if you have a trust minimized bridge. If you have a bridge, you can use the native token. If you don’t, like sovereign rollups, you have to use your own token.

### Other things discussed and scratch notes

Ethereum uses smart contracts that act as light nodes to execute transactions, so it’s not sovereign

But you can still have a trust minimized bridge (it’s enshrined meaning it doesn't have any special status in the system to dictate the rollup state), so they can be layer 2s. The bridge just becomes aware of the rollup state.

Counterparty protocol, look this up

Consensus security from the Layer 1, censorship resistance, light clients...

Ownership security, Bitcoin doesn’t have the capability to validate withdrawals on other chains

Blob space ethereum (deleting block space if not used)

Off chain data availability layers

Synchrony assumptions Bitcoin

Sovereign cluster of chains

Cosmos uses validator set to select the correct hard fork 

Mergemined & Federated Bridges
