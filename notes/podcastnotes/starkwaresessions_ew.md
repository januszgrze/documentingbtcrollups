From this [talk](https://www.youtube.com/watch?v=_hLvvZGST_E)

Taproot has this thing called [merkelized abstract syntex trees](https://www.google.com/search?q=merkelized+abstract+syntax+trees&biw=1041&bih=710&sxsrf=APwXEde0AtnAQYhpCVrRGbkfi-pzepoBEw%3A1679653840433&ei=0HsdZN2MGvH41sQPycuQ2AU&oq=merkelized+&gs_lcp=Cgxnd3Mtd2l6LXNlcnAQAxgAMgUIABCABDIGCAAQHhAKOgoIABBHENYEELADOgQIIxAnOggILhCKBRCRAjoICAAQigUQkQI6DgguEIAEEMcBENEDENQCOgUILhCABDoOCC4QigUQxwEQ0QMQkQI6BwguEIoFEEM6BwgAEIoFEEM6CgguEIoFENQCEEM6DgguEMcBENQCENEDEIAEOgsILhDHARDRAxCABDoNCC4QgAQQxwEQ0QMQCjoNCC4QgAQQxwEQrwEQCjoLCC4QgAQQxwEQ0QM6BwgAEIAEEAo6CAguEIAEENQCOgcILhCABBAKOgoILhCABBDUAhAKOgsILhCABBDHARCvAUoECEEYAFDlB1jPFmDcHmgDcAF4AIABlgGIAc4KkgEEMC4xMZgBAKABAcgBAsABAQ&sclient=gws-wiz-serp)

Taproot adoption hasn't been great. Can do some interesting things like Schnoor signatures and multi signatures. The multi signatures can look like a single signature theoretically could help privacy.

Ordinals system was created in December of last year. Is done on taproot. You can store arbitrary amounts of data on the Bitcoin blockchain.

Bitcoin has a programming language called Bitcoin script.

Some limitations:

Ordinals essentially invented this thing called CALLDATA, which Ethereum people are familiar with. Go further and call it BLOBSPACE

Storing data on Bitcoin is 75% cheaper than Ethereum (fact check).

Fee market on Bitcoin is very low. Not a lot you can do. Lack of MEV, on-chain DEXs, no arbitrage.

Blockspace is very cheap because of this.

For example, Trump NFT, 360kb of data cost $20 to store on Bitcoin. This is 7x cheaper than Bitcoin.

Sidebar: There's nothing on the Bitcoin roadmap, like pruning or history expiry, essentially throwing away old chain data so nodes can sync more effeciently.

Because this is so cheap to use, it's good to mess about with it now and see if it could be potentially problematic in future. If problematic, people could fix it now.

NFTs can be good because they can generate fees.

Back in the day, the idea was to build decentralized sidechains on Bitcoin. Was supposed to come from Blockstream and it never came.

Drivechains never happened either as people feared miner centralization.

Study's show the you can increase the throughput on Bitcoin 35x if you used a zk-rollup. However, it would take a bunch of softforks that we're not sure if we could get into Bitcoin.

But the idea, we use cheap proof-of-work blockspace and build sovereign rollup.

What is a sovereign rollup:

A layer 2 that uses the layer 1 as the mechanism for ordering blocks to create the order of transactions and guarantee data availability. So you don't have fraud proofs, or validity proofs, on the layer 1. All of this happens in the layer 2. You just get consensus and ordering from layer 1.

You could start building this now.
