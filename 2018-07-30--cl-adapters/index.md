---
title: Chainlink Adapters
subTitle: Consistently updated list of available and open-sourced Chainlink external adapters.
category: "confirmed"
cover: cover.jpg <!-- Don't touch this line -->
---

# External Adapters
External adapters are what make Chainlink easily extensible, providing simple integration of custom computations and specialized APIs. A Chainlink node communicates with external adapters via a simple REST API. ([src](https://github.com/smartcontractkit/chainlink/wiki/Glossary#external-adapter))

## Types of adapters that can exist on Chainlink network
1. Blockchain Adapters
> Bitcoin  
> IOTA  
> Hyperledger  
> IPFS  
2. Financial Adapters
> Stock price feeds  
> Interest rates, LIBOR, and other financial rates  
> Trigger external (off-chain) payments  
> Industry-Specific Adapters  
3. Weather
> Sports results  
> Political/Voting results  
> Shipping/Package tracking  
> IoT/RFID/Sensor results  
4. Miscellaneous Adapters
> Data manipulation  
> XML  
> Email notifications  
> SMS notifications  
> General serverless   
> Order a pizza  

## List of currently available Chainlink external adapters.
There aren't too many implemented adapters that you can get your hands on right now, except the ones created by the Linkpool Team. 
### [Asset Price Adapter](https://github.com/linkpoolio/asset-price-cl-ea)
External Adapter for Chainlink which aggregates prices of crypto assets from multiple exchanges based on a weighted average of their volume.
### [XML -> JSON Adapter](https://github.com/linkpoolio/xml-cl-ea)
This adapter allows for converting of XML API's into JSON. This allows ChainLink nodes to use API's which use XML as a markup. It's built in Go using go-json-rest.
### [Iota Adapter](https://github.com/linkpoolio/iota-cl-ea)
Iota adapter for Chainlink that currently supports the following IOTA API queries:
> broadcastAndStore  
> findTransactionObjects  
> getTransactionsObjects  
> getAccountData  
> getNodeInfo  
> sendTrytes  
