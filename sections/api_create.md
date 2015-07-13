# exchange_create

Should be called to deploy new `smart exchange` contract to ethereum network and to register it with given identifier.

## request params:

- **identifier**: unique 4 uppercase alphanumeric characters that are an exchange identifier
- **overwrite**: boolean that indicates, if we should create new exchange with given identifier if one already exists. True is unsafe.

## request example:

```json
{
  "id": 8,
  "jsonrpc": "2.0",
  "method": "exchange_create",
  "params": [
    "XROF",
    false
  ]
}
```

## using curl:

```bash
curl -X POST --data '{"id":8,"jsonrpc":"2.0","method":"exchange_create","params":["XROF", false]}' -H "Content-Type: application/json" http://localhost:8080
```

## response:

- **result** - address of the created exchange

## response example:

```json
{
  "jsonrpc": "2.0",
  "id": 8,
  "result": "0x209f728097e6ea54068c62b5b534c115b9c5d5b5"
}
```