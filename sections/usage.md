# Usage

Guide how to use `smart-exchange`.

### Start service

Before you start using `smart-exchange` you need to setup 2 options - `namereg` and `owner`. Look at configuration section for more details.

```bash
cd smart-exchange
npm install
node app.js
```

When using it in production environment I recommend using `pm2` as a process manager.

```bash
cd smart-exchange
pm2 start app.js
```

You can also install `smart-exchange` using npm

```bash
npm install smart-exchange -g
smart-exchange config.json # where config.json is full path to your configuration file
```

You can also use `smart-exchange` directly from your node application

```js
var se = require('smart-exchange');
```

### Create and register your exchange

After that you need to create your echange contract on the blockchain and register it in the namereg. It can be done with `exchange_create` method.

At this point, you have successfully deployed an exchange to the blockchain.

### Transfer funds from exchange

`echange_transfer` method can be used to do that. It will move the funds to desired address and create a log in transactions list.

### Transfer funds to exchange

You can use [this](http://ethchange.github.io/) static webpage to transer some funds from your eth address to the exchange. It expects unlocked geth node to be at port 8545.

### Get transactions list

We do not provide an API to notify about incoming transations. Although you can query for previous transactions using `exchange_transactions` method. We will let you know how many confirmations are considered safe during Frontier.

### Get transaction by hash

TODO

### Get exchange balance

`exchange_balance` method can be used to get exchange balance. Although it is not possible to query certain user balance, cause exchange contract do not store such information. It only stores list of transactions with values and from/to identifiers (similar to blockchain).

### See also:

[pm2](https://github.com/Unitech/pm2), [transfer funds page](https://ethchange.github.io)

