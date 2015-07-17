# Namereg

Namereg is a contract with key/value store and some permission system. The one that we will use, stores pairs of exchange identifiers and addresses. Exchanges will register in this namereg and will do a lookup in this registrar if they want to transfer funds to other institution (exchange).

We haven't decided yet what will be the permission system to add insitutuin to the namereg, but for tests we can use general version of namereg. It can be found in `eth-deploy/app/contracts/global_register.sol`

### Test environment

To deploy test namereg we need to run `embark deploy` inside `eth-deploy` directory. It may take few seconds, cause we will be waiting for contracts to be cofirnmed (mined).

```
> embark deploy

unning "deploy_contracts:development" (deploy_contracts) task
address is : 0x9c9855674488d1d14e3dfcf58ef0ce26df679447
address is : 0x9c9855674488d1d14e3dfcf58ef0ce26df679447
compiling app/contracts/global_register.sol
compiling app/contracts/simple_storage.sol
trying to obtain GlobalRegistrar address...
address is 0x44040da17453b2c56506547cec905d3479d26ecc
deployed GlobalRegistrar at 0x44040da17453b2c56506547cec905d3479d26ecc
trying to obtain NameRegister address...
address is 0xdae4b657bcac8100c8b213defe684951bc5e8ae6
deployed NameRegister at 0xdae4b657bcac8100c8b213defe684951bc5e8ae6
trying to obtain Registrar address...
address is 0xfbff4acda68fc813c4baa23c70c825b83d5408b1
deployed Registrar at 0xfbff4acda68fc813c4baa23c70c825b83d5408b1
trying to obtain owned address...
address is 0x699a60c02765cba41eeb82c03579539fec19feea
deployed owned at 0x699a60c02765cba41eeb82c03579539fec19feea
trying to obtain SimpleStorage address...
address is 0x6afc2e1ae7b3f7369b6f6829cef40e0ff8783ce1
deployed SimpleStorage at 0x6afc2e1ae7b3f7369b6f6829cef40e0ff8783ce1
address is 0x44040da17453b2c56506547cec905d3479d26ecc
address is 0xdae4b657bcac8100c8b213defe684951bc5e8ae6
address is 0xfbff4acda68fc813c4baa23c70c825b83d5408b1
address is 0x699a60c02765cba41eeb82c03579539fec19feea
address is 0x6afc2e1ae7b3f7369b6f6829cef40e0ff8783ce1
```

Please ignore for now, that so many contracts are being deployed. We are working on improving this process. The contract that we are intrested in is called `GlobalRegistrar` and it's address is **`0x44040da17453b2c56506547cec905d3479d26ecc`**

### See also:

[eth-deploy](https://github.com/debris/eth-deploy), [embark-blockchain](https://github.com/iurimatias/embark-blockchain), [geth](https://github.com/ethereum/go-ethereum)

