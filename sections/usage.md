# Usage

Guide how to use `smart-exchange`.

## Start service

Before you start using `smart-exchange` you need to setup 2 options - `namereg` and `owner`. Look at configuration section for more details.

```bash
cd smart-exchange
npm install
node app.js
```

## Create and register your exchange

After that you need to create your echange contract on the blockchain and register it in the namereg. It can be done with `exchange_create` method.

At this point, you have successfully deployed an exchange to the blockchain.

## Transfer funds from exchange

`echange_transfer` method can be used to do that. It will move the funds to desired address and create a log in transactions list.

## Transfer funds to exchange

TODO example webpage

## Get transactions list

We do not provide an API to notify about incoming transations. Although you can query for previous transactions using `exchange_transactions` method. We will let you know how many confirmations are considered safe during Frontier.

## Get transaction by hash

TODO

## Get exchange balance

`exchange_balance` method can be used to get exchange balance. Although it is not possible to query certain user balance, cause exchange contract do not store such information. It only stores list of transactions with values and from/to identifiers (similar to blockchain).
