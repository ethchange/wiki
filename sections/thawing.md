# After "Thawing" phase end

*this page is a draft*

There are few additional steps that are required to make IBAN transactions available.

1. We ("Ethereum Foundation") will create Exchange Namereg Contract. We won't own it in any way and we will not be able to alter it's state on different basis than anyone else. This Namereg Contract is called Fixed Fee Registrar and is available [here](https://github.com/ethereum/dapp-bin/blob/master/registrar/FixedFeeRegistrar.sol).
2. Once the contract is created, we will give it's address to the exchanges.
3. Exchanges will use `exchange_create` method to create their contract and register it in Namereg. 
    - registration in namereg will cost ~**69 ETH**
    - there will be new `smart_exchange` method called `exchange_disown` which will unregister exchange contract from namereg and transfer back **69 ETH** to exchange owner address.
4. We (Ethdev) will add new method to javascript library && geth console called `sendIBANTransaction`. This method will be used by users to transfer funds to exchange.
    - example:
    ```js
    eth.sendIBANTransaction(
        "0xb60e8dd61c5d32be8058bb8eb970870f07233155",
        "XE81ETHXREGGAVOFYORK",
        "0x10"
    )
    ```

