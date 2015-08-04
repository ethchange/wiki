# exchange_disown

Should be called to disown (unregister) exchange with given identifier.

### request params:

- **identifier**: unique 4 uppercase alphanumeric characters that are an exchange identifier

### request example:

```json
{
  "id": 8,
  "jsonrpc": "2.0",
  "method": "exchange_disown",
  "params": [
    "XROF"
  ]
}
```

### using curl:

```bash
curl -X POST --data '{"id":8,"jsonrpc":"2.0","method":"exchange_disown","params":["XROF"]}' -H "Content-Type: application/json" http://localhost:8545
```

### response:

- **result** true if exchange is unregistered

### response example:

```json
{
  "jsonrpc": "2.0",
  "id": 8,
  "result": true
}
```

### Errors:

| Name | Code |
| - | - |
| UNKNOWN_ERROR                     | **`100`** |
| IDENTIFIER_IS_INCORRECT           | **`101`** |
| IDENTIFIER_NOT_OWNED              | **`103`** |

### See also:

[errors](api_errors.md)
