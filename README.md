# SimpleStorage

## Uso

### Anvil

Corre el nodo de Ethereum local
```shell
$ anvil
```

### Deploy

Forma simple de deployment. Utiliza uno de los private keys generados por anvil. No utiliza scripts.
```shell
$ forge create SimpleStorage --private-key $ANVIL_PRIVATE_KEY
```

Deployment a traves de custom scripts al nodo local. Utiliza uno de los private keys generados por anvil y el rpc url de anvil.
```shell
$ forge script script/SimpleStorage.s.sol:DeploySimpleStorage --rpc-url $ANVIL_RPC_URL --private-key $ANVIL_PRIVATE_KEY --broadcast
```

Deployment a traves de custom scripts al nodo local. Utiliza un key store encriptado para guardar el private key.
Esto es una mejor practica de seguridad que pasar el private key en la terminal directamente o a traves de una variable de entorno.
```shell
$ forge script script/SimpleStorage.s.sol:DeploySimpleStorage --rpc-url $ANVIL_RPC_URL --account defaultKey --sender 0xf39Fd6e51aad88F6F4ce6aB8827279cffFb92266 --broadcast
```

### Cast

Traduce un valor hexadecimal a decimal. 
```shell
$ cast --to-base {hex} dec
```

Importa un private key al key store encriptado.
```shell
$ cast wallet import defaultKey --interactive
```

Envia una transaccion al contrato {address} en anvil llamando la funcion "store()" con el private key.
```shell
$ cast send {address} "store(uint256)" 123 --rpc-url $ANVIL_RPC_URL --private-key $ANVIL_PRIVATE_KEY
```

Llama la funcion "retrieve()" del contrato {address}. Por ser un view function no incurre costos de gas.
```shell
$ cast call {address} "retrieve()"
```

### Test

Corre los tests
```shell
$ forge test
```


### Format

Formatea el codigo.
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



## Documentation

https://book.getfoundry.sh/
