# SimpleStorage

## Uso

### Anvil

```shell
$ anvil
```

### Deploy

```shell
$ forge create SimpleStorage --private-key $ANVIL_PRIVATE_KEY
```

```shell
$ forge script script/SimpleStorage.s.sol:DeploySimpleStorage --rpc-url $ANVIL_RPC_URL --private-key $ANVIL_PRIVATE_KEY --broadcast
```

```shell
$ forge script script/SimpleStorage.s.sol:DeploySimpleStorage --rpc-url $ANVIL_RPC_URL --account defaultKey --sender 0xf39Fd6e51aad88F6F4ce6aB8827279cffFb92266 --broadcast
```

### Cast

```shell
$ cast --to-base {hex} dec
```

```shell
$ cast wallet import defaultKey --interactive
```

```shell
$ cast send {address} "store(uint256)" 123 --rpc-url $ANVIL_RPC_URL --private-key $ANVIL_PRIVATE_KEY
```

```shell
$ cast call {address} "retrieve()"
```

### Test

```shell
$ forge test
```


### Format

```shell
$ forge fmt
```

### Gas Snapshots

```shell
$ forge snapshot
```



### Help

```shell
$ forge --help
$ anvil --help
$ cast --help
```




## Foundry

**Foundry is a blazing fast, portable and modular toolkit for Ethereum application development written in Rust.**

Foundry consists of:

-   **Forge**: Ethereum testing framework (like Truffle, Hardhat and DappTools).
-   **Cast**: Swiss army knife for interacting with EVM smart contracts, sending transactions and getting chain data.
-   **Anvil**: Local Ethereum node, akin to Ganache, Hardhat Network.
-   **Chisel**: Fast, utilitarian, and verbose solidity REPL.

## Documentation

https://book.getfoundry.sh/
