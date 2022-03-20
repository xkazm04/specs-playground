# KB-Security

https://blog.openzeppelin.com/the-hitchhikers-guide-to-smart-contracts-in-ethereum-848f08001f05/

https://consensys.net/diligence/blog/2019/10/solidity-visual-auditor-extension-for-vs-code/
https://github.com/ConsenSys/mythril
https://github.com/smartbugs/smartbugs

## Best practices
- Be careful about external contract calls 
- Anyone can view private data in smart contracts


## Front running attacks
https://www.leewayhertz.com/best-practices-for-ethereum-smart-contract/

## Re-entrancy 
- 
https://solidity-by-example.org/hacks/re-entrancy/

1. Let's say that contract A calls contract B.
2. Reentracy exploit allows B to call back into A before A finishes execution.


- Ensure all state changes happen before calling external contracts
- Use function modifiers that prevent re-entrancy
- PullPayment - Best practice to send ether
- ReentrancyGuard