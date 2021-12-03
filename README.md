# nft-demo


### Completado

### Pendiente
- Automatizar usando docker file


## Entorno dockerizado

<!-- #region -->
Crear contenedor

```
sudo docker run --name solidity-sample \
    -v $HOME/sources/blockchain/solidity:/opt/solidity \
    -t ubuntu:20.04 sleep infinity
            
```


Configuración global

```
sudo apt-get update
sudo apt-get install -y nodejs npm vim
```


Configuración de node

```
cd /opt/solidity

npm install -g truffle
truffle init npm 

npm install @openzeppelin/contracts

perl -pi -e 's/0.8.10/0.8.3/g' npm/truffle-config.js 

```
<!-- #endregion -->

```python

```

## Creación del contrato


Creación del contrato: Desde la consola de truffle
```
mkdir -p npm/contracts
cp FemiToken.sol npm/contracts/FemiToken.sol

mkdir -p npm/migrations
cp 2_token_migration.js npm/migrations/2_token_migration.js

truffle development

## from the truffle shell
migrate
```


## Ejecución contrato


Ejecución del contrato
```
let token = await FemiToken.deployed();
token.mint(accounts[0]);  
token.transferFrom(accounts[0], accounts[1], 0);  
```

```python

```
