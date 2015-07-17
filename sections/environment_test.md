# Test environment

To setup test environment please go to `eth-deploy` repository and follow the steps there. `embark-blockchain` command will run `geth` client with proper configuration in the background.

### TL;DR

```bash
- git clone https://github.com/debris/eth-deploy
- cd eth-deploy
- npm install
- embark blockchain 
- embark deploy 
```

### Note

`embark-framework` uses `/tmp/embark/` as default directory to store blockchain. To prevent your data from being erased, I recomment changing this directory to something else. It can be done by altering `config/blockchain.yml` in `eth-deploy`.

### See also:

[eth-deploy](https://github.com/debris/eth-deploy), [embark-blockchain](https://github.com/iurimatias/embark-blockchain), [geth](https://github.com/ethereum/go-ethereum)

