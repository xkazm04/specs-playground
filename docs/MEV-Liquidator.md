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

#### Process
1. Start node server
2. Poll market and accounts with interval
3. Prepare stores

### Solend
[Solana lending protocol](https://github.com/solendprotocol/liquidator/blob/main/src/liquidate.ts)

#### Process
Run liquidator
1. Connect to cluster
2. getTokensOracle, getOblications, getReserves

- Do nothing if oblication is healthy
- Select repay token with highest market value
- Select the withdrawal collateral with highest market value
- Get wallet balance of selected borrow token
- Liquidate and redeem

#### Model
- Transaction instruction
  1. InitLendingMarket = 0,
  2. SetLendingMarketOwner = 1,
  3. InitReserve = 2,
  4. RefreshReserve = 3,
  5. DepositReserveLiquidity = 4,
  6. RedeemReserveCollateral = 5,
  7. InitObligation = 6,
  8. RefreshObligation = 7,
  9. DepositObligationCollateral = 8,
  10. WithdrawObligationCollateral = 9,
  11. BorrowObligationLiquidity = 10,
  12. RepayObligationLiquidity = 11,
  13. LiquidateObligation = 12,
  14. FlashLoan = 13,
  15. DepositReserveLiquidityAndObligationCollateral = 14,
  16. WithdrawObligationCollateralAndRedeemReserveLiquidity = 15,
  17. UpdateReserveConfig = 16,
  18. LiquidateObligationAndRedeemReserveCollateral = 17,

#### SC Liquidator
[ETH Smart contract liquidation ](https://github.com/aparnakr/LiquidatorBot)


