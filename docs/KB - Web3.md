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

It seems inevitable blockchain technologies knocking on the door with ambitions find a place in the world of development. Have you heard term **web3** and don't know what to expect? Let's find out :)

## What is web3

Web3 or Web 3.0 is described as next evolutionary step in the way how web application works:

- **web1** - Static running hosted on central storage
- **web2** - Dynamic apps running on central storage or multiple at the same time (cloud)
- **web3** - Dynamic apps running in decentralized publicly transparent network

Definition of Web 3.0 related with cryptocurrencies was firstly idealized by Ethereum (2nd largest cryptocurrency) in 2014 as *decentralized digital infrastructure* with core principals to be designed:

- **Trustless** - Not required support of trusted entity
- **Decentralized** - Running by peer-to-peer network
- **Permissionless** - No governing mediator 

![web3.png](https://stoplight.io/api/v1/projects/cHJqOjEyMDc0MQ/images/lXupgGDFcSk)
*https://academy.moralis.io/blog/what-is-web3-web-3-0-explained*

To achieve above paradigma, application has to run instead of traditional infrastructure and backend services rather on [**Smart contract platforms**](TBD link) with provided set of technical and economic mechanisms:

- How to motivate new peers to join network
- How to write and deploy web3 applications
- How to process transactions and scale them

### How it works
1. Come with **business idea**
2. **Choose platform/s** to work with 
3. **Write smart contract** in language required by platform. Test them (unit tests, testnet)
4. Write **UI** to smart contracts (React, Next, Svelte). User will interact with contract with blockchain wallet
5. **Deploy** contract with related tooling. Transaction fee will be required based on chosen platform.
6. Blockchain state machine will be updated after deployment and smart contracts become interactive, all its activity transparently stored on blockchain


![image.png](https://stoplight.io/api/v1/projects/cHJqOjEyMDc0MQ/images/enzsVZYK0po)


## Why to develop web3 apps

- Open new possibities and use cases into your portfolio
- Create existing web2 apps more effective in trustless manner
- Find job and make money, web3 resources are more valuable then gold

## Problems web3 apps could solve

- Bad product market fit
- Meaningless work
- Increased cost
- Unhappy clients
- Unsuccessful product

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

## Common Pitfalls of Web 3.0 development

- Lack of tooling and best practices
- Smart contracts built ineffectively to consume lot of gas fee to operate with
- Maturity of Solidity programming language allows security vulnerabilities needed to cover


## Resources for web3

- tools
- guides
- starters