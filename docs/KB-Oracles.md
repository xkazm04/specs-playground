# KB-Oracles

https://cointelegraph.com/explained/blockchain-oracles-explained

https://www.gemini.com/cryptopedia/what-is-chainlink-and-how-does-it-work

https://www.investopedia.com/chainlink-link-definition-5217559

TBD Blockchain Oracle problem definition
https://chain.link/education/blockchain-oracles
https://cointelegraph.com/blockchain-for-beginners/what-is-a-blockchain-oracle-and-how-does-it-work



## What is
Oracles are bridges between traditional web world and decentralized Web 3.0 ecosystem. Basically network of computers gathers various data sources as a replacement of traditional API and provides data into marketplace where dozens of blockchain network could consume it trustless without fear data could be tamper.

Mechanisms TBD rozvést
- Reputation system
- Motivation system
- Tamper proof 

Chainlink picture 
![image.png](https://stoplight.io/api/v1/projects/cHJqOjEyMDc0MQ/images/7mMsXG3bkM0)


Bridge between traditional and web3 world 
- Decentralized API

## Why might want
Use cases
- Price feed
- Sports betting
- Randomness generator

## Problems solved
- Trust
- Double-spending attacks
- Blockchain oracle problem

## How to implement
Choose oracle provider based blockchain network - most chains covered by Chainlink
Install dependencies
Use prepared Chainlink interfaces into your smart contract


Solidity example

```Solidity
// SPDX-License-Identifier: MIT
pragma solidity ^0.8.7;

import "@chainlink/contracts/src/v0.8/interfaces/AggregatorV3Interface.sol";

contract PriceConsumerV3 {
    AggregatorV3Interface internal priceFeed;

    /**
     * Network: Kovan
     * Aggregator: ETH/USD
     * Address: 0x9326BFA02ADD2366b30bacB125260Af641031331
     */
    constructor() {
        priceFeed = AggregatorV3Interface(0x9326BFA02ADD2366b30bacB125260Af641031331);
    }

    /**
     * Returns the latest price
     */
    function getLatestPrice() public view returns (int) {
        (
            /*uint80 roundID*/,
            int price,
            /*uint startedAt*/,
            /*uint timeStamp*/,
            /*uint80 answeredInRound*/
        ) = priceFeed.latestRoundData();
        return price;
    }
}
```


## Common pitfalls
- Cost
- Market monopolly

## Resources
Chainlink
https://betterprogramming.pub/what-is-a-blockchain-oracle-f5ccab8dbd72

https://docs.chain.link/docs/architecture-overview/
https://cointelegraph.com/blockchain-for-beginners/what-is-a-blockchain-oracle-and-how-does-it-work
https://medium.com/emiswap/the-ultimate-guide-on-blockchain-oracles-b9dac589edba