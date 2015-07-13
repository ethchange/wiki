# Configuration

- **contract** - path to the contract which should be used on exchange creation.
- **contract_name** - name of exchange contract which should be used.
- **jsonrpc_host** - native client jsonrpc host, eg. `localhost`
- **jsonrpc_port** - native client jsonrpc port, eg. `8545`
- **exchange_interface** - smart-exchange jsonrpc interface. Available options `http` && `tcp`
- **exchange_port** - port for smart-exchange jsonrpc, eg. `8080`
- **owner** - address of unlocked account which from which exchange is being created, eg. `0xe30b49f729469c3b8ffef495b31e4d4e790a1a46`
- **namereg** - address of namereg which should be used to register identifiers, eg. `0xb6eab56fb20feba03bcdbd7789cc24740f6b90ee`. You can also use `default` *actually default is TODO*.

example: 

```json
{
    "contract": "lib/contract/SmartExchange.sol",
    "contract_name": "SmartExchange",
    "jsonrpc_host": "localhost",
    "jsonrpc_port": "8545",
    "exchange_interface": "http",
    "exchange_port": 8080,
    "owner": "0xe30b49f729469c3b8ffef495b31e4d4e790a1a46",
    "namereg": "0xb6eab56fb20feba03bcdbd7789cc24740f6b90ee"
}
```