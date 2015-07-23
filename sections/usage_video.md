# Video tutorial

[![asciicast](https://asciinema.org/a/19ywf3hkhwq5j3y2bs2oefskl.png)](https://asciinema.org/a/19ywf3hkhwq5j3y2bs2oefskl)

On the video you can see the following actions:

- **exchange_create** - creates new exchange
- **exchange_address** - let's check exchanges address
- **exchange_balance** - let's check exchange balance, expected 0
- **eth_accounts**  - obtain users list, required to set `from` in `eth_sendTransaction`
- **eth_sendTransaction** - send 'raw' transaction. Exchange will receive it as AnonymousDeposit
- **exchange_transactions** - returns 1 AnonymousDeposit
- **exchange_balance** - returns 15
- **exchange_transfer** - between two identifiers inside exchange
- **exchange_transfer** - transfer funds to normal ethereum address
- **eth_balance** - returns 9
- **exchange_transactions** - returns 4 transactions: 1 AnonymousDeposit, 1 Deposit, 1 Transfer, 1 IcapTransfer

