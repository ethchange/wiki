# smart-exchange 

[smart-exchange](https://github.com/ethchange/smart-exchange) is a script that can be used to deploy and manage ethereum exchange service which is compatible with [ICAP](https://github.com/ethereum/wiki/wiki/ICAP:-Inter-exchange-Client-Address-Protocol) 

`smart-exchange` **doesn't store account balances on or off the chain**. It just provides convenient way to store list of transactions with custom identifiers on the blockchain. Identifiers which don't need to be created (like bitcoin accounts) and whose identity is known only to the exchange.

An exchange **doesn't have to deal with smart contracts** directly. `smart-exchange` is a wrapper around smart contract and exposes easy to use JSON-RPC api.
