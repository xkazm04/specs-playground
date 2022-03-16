---
slug: web3_development
stages:
  - development
short_description: Code Coverage measures the percentage of source code lines that are covered by automated tests. If you have 90% CC, it means that 10% of the source code is not being tested at the moment.
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

# Web3

**TL;DR**

It seems inevitable blockchain technologies knocking on the door with ambitions find a place in the world of development. Have you heard term **web3** and don't know what to expect? Let's find out :)

## What is web3

Definition of Web 3.0 related with cryptocurrencies was firstly idealized by Ethereum (2nd largest cryptocurrency) in 2014 as *decentralized digital infrastructure* with core principals to be designed:

- **Trustless** - Not required support of trusted entity
- **Decentralized** - Running by peer-to-peer network
- **Permissionless** - No governing mediator 

**TBD image**

To achieve above paradigmas web application has to run instead of traditional infrastructure and backend services rather on [**Smart contract platforms**](TBD link), they provide set of mechanisms:

- How to motivate new peers to join network
- How to write and deploy web3 applications
- How to process transactions and scale them

### How it works
- Browser
- Wallet 
- 

### Smart contract platforms
Similarly to traditional web development your first decision would be probably to choose the right tech-stack where to start, market offers today dozens of platforms to use, different in criterias:

- User adoption
- Decentralization
- Development tooling maturity
- Smart contract programming language


## Why to develop web3 apps

- Opens new possibities and use cases into your portfolio
- Allows to adapt new technology area trendy in current decade

## Problems web3 apps could solve

Current decentralization and maturity level of whole ecosystem does not enable yet to use full potential Web 3.0 promises on paper - which should be:

- Censorship
- TBD Power from corporate entities to peer networks
- [Meaningless work](/problems/meaningless-work)

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

## Common Pitfalls of the Code Coverage

- Developers write useless tests to reach 100% CC.
- A developer corrects the functionality but does not correct the test. That means that a wrong test can fool the CC.
- A deveoper writes new code and applies wrong tests. The CC declines.

## Resources for the Code Coverage

- tools
- guides
- starters