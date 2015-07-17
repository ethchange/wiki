# exchange_balance

Should be called to check the balance of `smart exchange` with given identifier.

### request params:

- **identifier**: unique 4 uppercase alphanumeric characters that are an exchange identifier

### request example:

```json
{
  "id": 8,
  "jsonrpc": "2.0",
  "method": "exchange_balance",
  "params": [
    "XROF"
  ]
}
```

### using curl:

```bash
curl -X POST --data '{"id":8,"jsonrpc":"2.0","method":"exchange_balance","params":["XROF"]}' -H "Content-Type: application/json" http://localhost:8080
```

### response:

- **result** exchange balance

### response example:

```json
{
  "jsonrpc": "2.0",
  "id": 8,
  "result": "0"
}"
```

### Errors:

| Name | Code |
| - | - |
| UNKNOWN_ERROR                     | **`100`** |
| IDENTIFIER_IS_INCORRECT           | **`101`** |
| IDENTIFIER_NO_ADDRESS             | **`105`** |

### See also:

[errors](api_errors.md)
