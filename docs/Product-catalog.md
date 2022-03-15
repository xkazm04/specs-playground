# Product catalog

## Table of parameters

Column | Data type | Description | Example
---------|----------|---------|-------
 name | string|  Short service name | Mint NFT
 description| string | One sentence description | Increase supply of non-fungible token.
 operation | string | unique operationId of service | mintNft 
 endpoint | string | service endpoint | /nft/mintNFt 
 category | enum | logical category group| nft 
 subcategory | string | detail service categorization| Token operations 
 supported | object | JSON with supported chains| {"ADA":"true"} 
 docs | string | link to API docs| https://docs.tatum.io/rest/smart-contracts/mint-nft 
 credit | string | Tatum credit evaluation | 5 
 free | boolean | Credit type consumed| false 

### Category
Enum represents logical categories Dev portal is working with inside its content:

Category| Description | Enum value
---------|----------|---------
 `Blockchain` | Native transactions, get data, generate account | blockchain
 `Fungible` | ERC20 management | fungible
 `Multitoken` | ERC1155 management | multi
 `NFT` | ERC721 management | nft
 `NFT Marketplace` | NFT Marketpalce listings, auctions | marketplace
 `Storage` | Blockchain/IPFS storage | storage
 `Virtual accounts` | Private Ledger services | virtual
 `Exchange` | Build centralized exchange | exchange
 `Custody` | Security services, KMS | custody
 `Subscriptions` | Notification API, Alerts | subscriptions

### Supported chains
JSON with supported blockchains per [table](https://docs.tatum.io/rest/getting-started/supported-blockchains)

Adding chain into json will secure display in Dev portal related components:
```json
{
  "ADA": true,
  "BSC": true,
  "EGLD": true,
  "ETH": true,
  "FLOW": true,
  "ONE": true,
  "KCS": true,
  "KLAY": true,
  "POLYGON": true,
  "TRON": true
}
```

Related components:
- [Main page ](url)-> Service overview -> Link
- [FAQ page](url)
- [Internal](url) overview

### Free type
Credit type consumed:
- `true` - **Free** credit limit used
- `false` - **Pay as you go** credit limit used
