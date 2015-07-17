# Owner

Address of unlocked account which from which exchange is being created. This account should also have positive balance.

### Test environment

If you are running `eth-deploy` to create your test environment. You can get just copy'n'paste an account address from logs.

```
> embark-blockchain

Running "blockchain:development" (blockchain) task
running: geth --datadir="/tmp/embark" --logfile="/tmp/embark.log" --port 30303 --rpc --rpcport 8101 --networkid 62785 --rpccorsdomain "*" --minerthreads "1" --mine --maxpeers 0 --password config/password account list
Fatal: Could not list accounts: no keys in store
Fatal: Could not list accounts: no keys in store
running: geth --datadir="/tmp/embark" --logfile="/tmp/embark.log" --port 30303 --rpc --rpcport 8101 --networkid 62785 --rpccorsdomain "*" --minerthreads "1" --mine --maxpeers 0 --password config/password account new
Address: {9c9855674488d1d14e3dfcf58ef0ce26df679447}
running: geth --datadir="/tmp/embark" --logfile="/tmp/embark.log" --port 30303 --rpc --rpcport 8101 --networkid 62785 --rpccorsdomain "*" --minerthreads "1" --mine --maxpeers 0 --password config/password --unlock 9c9855674488d1d14e3dfcf58ef0ce26df679447 js node_modules/embark-framework/js/mine.js
I0717 08:58:35.709480   55138 backend.go:301] Protocol Versions: [61 60], Network Id: 62785
I0717 08:58:35.709975   55138 backend.go:311] Blockchain DB Version: 3
...
```

Account address is set to **`9c9855674488d1d14e3dfcf58ef0ce26df679447`**.


### See also:

[eth-deploy](https://github.com/debris/eth-deploy), [embark-blockchain](https://github.com/iurimatias/embark-blockchain), [geth](https://github.com/ethereum/go-ethereum), [managing-your-accounts](https://github.com/ethereum/go-ethereum/wiki/Managing-your-accounts)

