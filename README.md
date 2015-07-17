# smart-exchange 

`smart-exchange` is a script that can be used to deploy and manage ethereum exchange service. This exchange service implements `ICAP` protocol.

`smart-exchange` **doesn't store account balances on or off the chain**. It just provides convenient way to store list of transactions with custom identifiers on the blockchain. Identifiers which don't need to be created (like bitcoin accounts) and whose identity is known only to the exchange.

`smart-exchange` is a stateless wrapper around smart contract and exposes easy to use JSON-RPC api, so an exchange **doesn't have to deal with smart contracts** directly. 

### See also:

[smart-exchange](https://github.com/ethchange/smart-exchange), [ICAP](sections/icap.md)
