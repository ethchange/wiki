# exchange_address

Should be called to get exchange address.

### request params:

- **identifier**: unique 4 uppercase alphanumeric characters that are an exchange identifier

### request example:

```json
{
  "id": 8,
  "jsonrpc": "2.0",
  "method": "exchange_address",
  "params": [
    "XROF"
  ]
}
```

### using curl:

```bash
curl -X POST --data '{"id":8,"jsonrpc":"2.0","method":"exchange_address","params":["XROF"]}' -H "Content-Type: application/json" http://localhost:8545
```

### response:

- **result** - address of the exchange

### response example:

```json
{
  "jsonrpc": "2.0",
  "id": 8,
  "result": "0x209f728097e6ea54068c62b5b534c115b9c5d5b5"
}
```

### Errors:

| Name | Code |
| - | - |
| UNKNOWN_ERROR                     | **`100`** |
| IDENTIFIER_IS_INCORRECT           | **`101`** |

### See also:

[errors](api_errors.md)
