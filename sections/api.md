# API

### Overview

[JSON](http://json.org/) is a lightweight data-interchange format. It can represent numbers, strings, ordered sequences of values, and collections of name/value pairs.

[JSON-RPC](http://www.jsonrpc.org/specification) is a stateless, light-weight remote procedure call (RPC) protocol. Primarily this specification defines several data structures and the rules around their processing. It is transport agnostic in that the concepts can be used within the same process, over sockets, over HTTP, or in many various message passing environments. It uses JSON ([RFC 4627](http://www.ietf.org/rfc/rfc4627.txt)) as data format.

### Methods

`smart-exchange` extends ethereum's [JSON-RPC API](https://github.com/ethereum/wiki/wiki/JSON-RPC) with following methods:

- `echange_create`
- `echange_transfer`
- `exchange_transaction`
- `exchange_transactions`
- `exchange_balance`

These methods are described on the next pages.
