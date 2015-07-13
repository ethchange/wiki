# Production environment

You just need to geth node with:

- an account
  ```bash
  geth account new
  ```

- unlocked account, jsonrpc server on, eg:
  ```bash
  geth --rpc --rpcport 8101 --rpccorsdomain "*"
       --password config/password # path to your file with pwd
       --unlock 2b7f9c3528a7a210297f1afe81be68dc9f295297 # an account to unlock
  ```
