---
title: Microsoft Speculation
subTitle: Project Bletchley, Cryptlets and Chainlink
category: "speculation"
cover: cover.jpg
---

Microsoft introduced Project Bletchley as their take in blockchain space. In short it is Microsoft's vision for an open, modular blockchain fabric powered by Azure. What's more interesting to us, however, is its connections to Chainlink.

# N.1 Sergey at NYC meetup
[Sergey states it himself CL & Microsoft are working together in this video](https://youtu.be/ytv8U0bejPA?t=46m2s)
The quote `We're proud to say we're working with them` is reference to the Bletchly/IC3 logos on the slide.

# N.2 SGX and Enclaves
This is more open to interpretation as any one could use SGX for something like this, but there's a lot of discussion around it which points directly to how ChainLink leverages SGX and TownCrier, for example:

> Secure IP protected algorithms but still share with the blockchain network: i.e. derivative pricing algorithm that multiple counter parties agree to use for a contract, but the actual algorithm remains secret, but attested.

So this is saying, when you create a cryptlet you can keep the logic for how the output is calculated private, but yet is still agreeable by multiple parties.

Again, this is exactly how Chainlink works. You create a "Chainlink" on the platform, and that Chainlink can be agreed to by multiple parties which can see the logic for how that price is calculated. Once it's then agreed, then all that logic is kept private within enclaves in SGX.

# N.3 Non-SmartContract Blockchain Platforms:

> For non SmartContract blockchains (UTXO), Cryptlets can be called with adaptors that perform the functions that the CryptoDelegate would in a SmartContract virtual machine, using Opcodes, etc.

This is statement is basically saying, any non-SmartContract platform is still supported by using adaptors to interact with that given Blockchain. This is exactly how Chainlink works. For example, it's initial implementation only includes Ethereum, and other chains will be supported later on by the development of core-adaptors. These adaptors are currently implemented and working on the current product @ http://create.smartcontract.com

# Cryptlet JSON Schema
This is an exact JSON schema fit (other than title) to the Chainlink Adaptor JSON found here: https://github.com/smartcontractkit/schemas/blob/master/schemas/adapter_schema.json
```json
{
    "title": "Cryptlet Schema",
    "type": "object",
    "properties": {
        "name": {
            "type": "string"
        },
        "publicKey": {
            "type": "string"
        },
        "config": {
            "description": "describe what Cryptlet does",
            "isolation": "boolean",
            "...":
        }
    },
    "required": ["name", "publicKey"]
}
```

# Marley Gray
The main contributor and principle architect for project Bletchley at Microsoft Marley Grey has [shared the stage with Sergey in the past](https://www.meetup.com/EthereumSiliconValley/events/241517216/)
[In his interview in January, he talks about the *Oracle Problem* in the context of ESK.](https://www.watchfintechtv.com/video/blockchain-business-disruptor-or-opportunity)
> Most contracts don't operate in a vacuum, they have to interact with market data, interest rates, etc... With smart contracts today there's no way for them to interact with this real-time market data. It's going to take a while to get there, but the first step's made

# Microsoft Azure Dev
[Aleksey Klintsevich](https://github.com/aklintsevich) has also been contributing to the chainlink code.

This is it for now. You can add your own findings to this post [from our GitHub]()