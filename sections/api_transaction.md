# exchange_transaction

Should be called to get a single transaction by transaction hash

### request params:

- **identifier**: unique 4 uppercase alphanumeric characters that are an exchange identifier
- **transactionHash**: 32 bytes length transaction hash

### request example:

```json
{
  "id": 8,
  "jsonrpc": "2.0",
  "method": "exchange_transactions",
  "params": [
    "XROF",
    "0xacf64bd586a847523086882c82c4cff6d77b1a753ea28c164046e37f3606583c"
  ]
}
```

### using curl:

```bash
curl -X POST --data '{"id":8,"jsonrpc":"2.0","method":"exchange_transactions","params":["XROF", "0xacf64bd586a847523086882c82c4cff6d77b1a753ea28c164046e37f3606583c"]}' -H "Content-Type: application/json" http://localhost:8545
```

### response:

- **result** transaction log

### response example

```json
{
  "jsonrpc": "2.0",
  "id": 8,
  "result": {
      "address": "0x9b173b6fab888af1b5eff49bf34c7aaebf58673f",
      "blockNumber": 55,
      "logIndex": 0,
      "blockHash": "0x0000000000000000000000000000000000000000000000000000000000000000",
      "transactionHash": "0xacf64bd586a847523086882c82c4cff6d77b1a753ea28c164046e37f3606583c",
      "transactionIndex": 0,
      "event": "Deposit",
      "args": {
        "from": "0x275ac21e0b9383dcc0fa0fc4ecf7bf1ec7c4bba9",
        "to": "0x4d4152454b4f464b4b0000000000000000000000000000000000000000000000",
        "value": "15000"
      }
    }
}
```

### Errors:

| Name | Code |
| - | - |
| UNKNOWN_ERROR                     | **`100`** |
| IDENTIFIER_IS_INCORRECT           | **`101`** |
| IDENTIFIER_NO_ADDRESS             | **`105`** |

### See also:

[errors](api_errors.md)

