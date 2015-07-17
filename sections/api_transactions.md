# exchange_transactions

Should be called to get list of exchange's transactions.

## request params:

- **identifier**: unique 4 uppercase alphanumeric characters that are an exchange identifier
- **options**: may contain additional fields (fromBlock, toBlock), that should be used to filter exchange transactions

## request example:

```json
{
  "id": 8,
  "jsonrpc": "2.0",
  "method": "exchange_transactions",
  "params": [
    "XROF",
    {
      "fromBlock": 100
    }
  ]
}
```

## using curl:

```bash
curl -X POST --data '{"id":8,"jsonrpc":"2.0","method":"exchange_transactions","params":["XROF", {"fromBlock": 100}]}' -H "Content-Type: application/json" http://localhost:8080
```

## response:

- **result** array of transaction logs

## response example:

```json
{
  "jsonrpc": "2.0",
  "id": 8,
  "result": [
    {
      "address": "0x9b173b6fab888af1b5eff49bf34c7aaebf58673f",
      "blockNumber": 55,
      "logIndex": 0,
      "blockHash": "0x0000000000000000000000000000000000000000000000000000000000000000",
      "transactionHash": "0x26cbc502a25df0a8c834b7eab0417df9c94e612ea02778a05020f219b3a5f0d3",
      "transactionIndex": 0,
      "event": "Deposit",
      "args": {
        "from": "0x275ac21e0b9383dcc0fa0fc4ecf7bf1ec7c4bba9",
        "to": "0x4d4152454b4f464b4b0000000000000000000000000000000000000000000000",
        "value": "15000"
      }
    }
  ]
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

### TODO:

- `fromBlock`, `toBlock` should be block hashes instead of block numbers
- validation of `fromBlock` && `toBlock`
