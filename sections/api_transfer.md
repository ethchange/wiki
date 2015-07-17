# exchange_transfer

Should be called to transfer funds from exchange's client to other address / institution. Might be also used for internal transfers.

## request params:

- **identifier**: unique 4 uppercase alphanumeric characters that are an exchange identifier
- **from**: unique user identifier, 9 alphanumeric characters.
- **to**, string which is one of:
    - **address**, ethereum address, 20 bytes in base 16 representation
    - **direct iban**, 34 alphanumeric characters, https://github.com/ethereum/wiki/wiki/ICAP:-Inter-exchange-Client-Address-Protocol#direct
    - **indirect iban**, 20 alphanumeric characters, https://github.com/ethereum/wiki/wiki/ICAP:-Inter-exchange-Client-Address-Protocol#indirect
    - **unique userid**, 9 alphanumeric characters
- **value**: value that should be sent

## request example:

```json
{
  "id": 8,
  "jsonrpc": "2.0",
  "method": "exchange_transfer",
  "params": [
    "XROF",
    "GAVOFYORK",
    "0xdc167599eeef974dcbdc6c49da98c42ac9e1c64b",
    6
  ]
}
```

## using curl:

```bash
curl -X POST --data '{"id":8,"jsonrpc":"2.0","method":"exchange_transfer","params":["XROF", "GAVOFYORK", "0xdc167599eeef974dcbdc6c49da98c42ac9e1c64b", 6]}' -H "Content-Type: application/json" http://localhost:8545
```

## response:

- **result** - transaction hash

## response example:

```json
{
  "jsonrpc": "2.0",
  "id": 8,
  "result": "0x462602d51f5c4db38bd419529fd7a206735cf497a433eb81134fcecc910757e2"
}
```

### Errors:

| Name | Code |
| - | - |
| UNKNOWN_ERROR                     | **`100`** |
| IDENTIFIER_IS_INCORRECT           | **`101`** |
| IDENTIFIER_NOT_OWNED              | **`103`** |
| IDENTIFIER_NO_ADDRESS             | **`105`** |
| FROM_IS_INCORRECT                 | **`110`** |
| TO_IS_INCORRECT                   | **`111`** |
| TO_IDENTIFIER_NO_ADDRESS          | **`112`** |

### See also:

[errors](api_errors.md)
