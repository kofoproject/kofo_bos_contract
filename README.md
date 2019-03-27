# KOFO EOS contract at  [atomicswap/](https://github.com/kofoproject/kofo_bos_contract/tree/master/atomicswap)

#### Compile contract
```bash
  eosio-cpp -abigen atomicswap/atomicswap.cpp -o atomicswap.wasm
```

#### Deploy contract
```bash
 cleos set contract kofobos.ac  ./atomicswap -p kofobos.ac
```
#### Permission
```bash
cleos set account permission receiver.ac active '{"threshold": 1,"keys": [{"key":${receiver.ac public key}, "weight":1}],"accounts": [{"permission":{"actor": "kofobos.ac","permission":"eosio.code"},"weight":1}]}' owner -p kofobos.ac@owner
```
