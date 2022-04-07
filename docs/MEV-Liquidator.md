# MEV-Liquidator

## Why? 
extract value from liquidated (smaller protocols)


## How?
Script (JS, TS)

### Dydx
[Dydx liquidator](https://github.com/dydxprotocol/liquidator/blob/master/src/index.ts)
#### Client
1. Get liquidatable accounts

```json
  const { accounts } = await request({
    method: 'GET',
    uri: `${process.env.DYDX_URL}/v1/accounts`,
    json: true,
    qs: {
      isLiquidatable: true,
    },
  });
  return { accounts };
}
```

2. Get expired accounts
```json
  const { accounts } = await request({
    method: 'GET',
    uri: `${process.env.DYDX_URL}/v1/accounts`,
    json: true,
    qs: {
      isExpired: true,
    },
  });
    return { accounts };
```

3. Get solo markets
```json
  const { markets } = await request({
    method: 'GET',
    uri: `${process.env.DYDX_URL}/v1/markets`,
    json: true,
  });
  return { markets };
```
#### Helper
1. GetLatestBlock
2. Liquidate account
3. Liquidate expired account
4. Proxy liquidate

#### Transaction helpers
- isDuplicateTxError
- isTxFailureError

#### Libraries
- getPriceUpdater
- gasPrice
- liquidationStore
- marketStore
- logging

### Process
1. Start node server
2. Poll market and accounts with interval
3. Prepare stores

