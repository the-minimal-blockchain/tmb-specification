# The Minimal Blockchain Specification

## Motivation

I hope a blockchain system does not depend on a linked-like data structure.

I hope a blockchain system does not depend on some consensus algorithm.

I hope a blockchain system does not depend on smart contracts.

I hope a blockchain system does not depend on token rewards.

I want to implement a minimal blockchain that is valuable by its simplicity, cleanliness code. It will have as few third-party modules as possible.

And it can be implemented by different programming languages, all implementation will follow the following design.

## Identity

Nodes have no identities because all data are shared.

## Network

The network departs into two parts.

One is block data communication network, that contains a node's dial or some message interactive, implement by TCP-likes protocol, it can be scaling with TLS or other cryptographic cases easy. 

Another one is the user-side API network, implement by HTTP-likes protocol that could accept user's operation.

## Consensus

The consensus mechanism will implemented based on:

- [A consensus mechanism based on "egocentrism"](https://smallyu-net.translate.goog/2021/10/29/%E4%B8%80%E7%A7%8D%E5%9F%BA%E4%BA%8E%E2%80%9C%E8%87%AA%E6%88%91%E4%B8%AD%E5%BF%83%E4%B8%BB%E4%B9%89%E2%80%9D%E7%9A%84%E5%85%B1%E8%AF%86%E6%9C%BA%E5%88%B6/?_x_tr_sch=http&_x_tr_sl=auto&_x_tr_tl=en&_x_tr_hl=en-US&_x_tr_pto=nui)
- [Consensus Mechanism for Randomly Confirming Blocks](https://smallyu-net.translate.goog/2022/09/25/%E9%9A%8F%E6%9C%BA%E7%A1%AE%E8%AE%A4%E5%9D%97%E7%9A%84%E5%85%B1%E8%AF%86%E6%9C%BA%E5%88%B6/?_x_tr_sch=http&_x_tr_sl=auto&_x_tr_tl=en&_x_tr_hl=en-US&_x_tr_pto=nui)

## Storage

The JSON format block data file named [blockNumber].json will be stored in a local folder.

Block data defined as:

```text
{
    prev: string,
    height: number
    payload: [{
        key: string,
        key1: string
    },
    {
        key2: string
    }]
}
```

## Documents

Reference the documents part in [the-minimal-blockchain/tmb-golang](https://github.com/the-minimal-blockchain/tmb-golang#Documents).

## FAQ

### Why this project?

If you want to start at blockchain technology but are too difficult to start it with Bitcoin or Ethereum, you will need the simplest project that contains key parts of the blockchain.

### Is this project stupid?

Maybe... Yes, it seems no actual value. I know some similar projects same as "minimal blockchain" don't get much focus, just like this project. I also understand the value of writing some articles is larger than the value of coding. But I want to do something, deposit I need to spend so much time on it.

### What progress now?

It is in progress. Due to the above question's reason, I would not complete it quickly, because I have no any reward on it. I just push its progress slowly when I have time and mood.

