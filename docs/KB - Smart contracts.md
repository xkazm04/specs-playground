---
slug: smart_contracts
stages:
  - development
  - deployment
short_description: ... TBD
tags:
  - web3
  - blockchain
keywords:
  - web3
  - blockchain
  - coding
  - programming
author_github_username: xkazm04
---

# Smart contracts

## What is smart contract

Concept of smart contracts represents piece of deployed code which is able to self-execute function in trustless manner under specific conditions. This "law" defined by code transparently allows to interact under **immutable** conditions - once smart contract is deployed in blockchain network it cannot be manipulated again.

Writing smart contracts requires condition to know basics of specific programming languages which might differ per blockchain network currently used in market.

Here is the list of popular blockchains and language in which their smart contracts could be developed

Blockchain| Languages | Total value locked in protocol*
---------|----------|---------
 Ethreum | Solidity | $116.07b
 Terra Luna | Rust | $25.42b
 BNB (Binance smart chain) | Solidity | $11.91b
 Avalanche | Solidity | $10.99b
 Solana | Rust | $6.96b

 *TVL dated to 3/22022


### How it works
![image.png](https://stoplight.io/api/v1/projects/cHJqOjEyMDc0MQ/images/f5ykbtyzagA)

Similarly to traditional web development your first decision would be probably to choose the right tech-stack where to start, market offers today dozens of platforms to use, different in criterias:

- User adoption
- Decentralization
- Development tooling maturity
- Smart contract programming language

1. Choose smart contract platform to work with
2. Install dependencies and related tooling to write & deploy smart contract
- Help yourself with frameworks (**Truffle**, **Hardhat**, **Brownie**)
- Don't hesitate to reuse already written contracts (OpenZeppelin, Etherscan)
- Select comfortable IDE (Remix, Visual Studio Code, Atom)
3. Write smart contract in programming language based on used platform 
4. Test smart contract functions
- Cover with unit tests (**Mocha**)
- Build local dev environment with tools like **Ganache**
- Access testnet environment via Alchemy, Infura
- Ensure functions cannot be exploited (Solidity Visual Developer)


## Why to develop smart contracts

Use cases 

- Token
- NFT
- Decentralized finance DeFi
- Voting
- Insurance
- Decentralized computing

- Opens new possibities and use cases into your portfolio
- Allows to adapt new technology area trendy in current decade

## Problems web3 apps could solve

Censorship ... TBD based on what written 

## How to Implement web3 apps

- Tech stack (Platform, language)
- Tooling (testnet, mainnet)
- Tests
- Frontend/SC ->

Set up the library for your software and run it under a controlled environment. Use a CC tool to map every executed function.

There are a lot of CC tools you can use, for each programming language. For example:

- Java: [jUnit](https://junit.org/junit5/), [Cobertura](http://cobertura.github.io/cobertura/), or [JaCoCo](https://www.jacoco.org/)
- JavaScript: [istanbul](https://istanbul.js.org/), or [JSCover](http://tntim96.github.io/JSCover/)
- PHP: [Clover](http://openclover.org/), or [PHPUnit](https://phpunit.de/)
- Python: [coverage.py](https://pypi.org/project/coverage/)
- Ruby: [SimpleCov](https://github.com/colszowka/simplecov)
- Scala: [Scoverage](http://scoverage.org/)

Update the tests if there are no areas of code that have not been exercised. Developers can check CC reports to advise additional tests to increase the CC.
**Important:** The process can slow down the application so it is not recommended to do it in production.

## Common Pitfalls of smart contracts

- Financial apps vulnerable to security exploits
- Tooling

## Best practices
- Be ready for failure (upgrade strategy)
- Rollout through testing contracts
- Unit tests
- Keep smart contracts simple and modularize
- Prefer clarity over performance
- Stay updated
- Be aware how gas costs works

## Fundamental tradeoffs
- Duplication vs Reusing 
- Monolithic (readable) vs Modular (optimal) architecture
- Rigid (safe) vs Upgradable contracts




## Resources for web3

- openZeppelin
- 
- starters