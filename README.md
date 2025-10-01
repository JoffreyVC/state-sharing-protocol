## Installation
 **You will need Go 1.23, JQ and Bazel installed**. 
 
```bash
git clone --recursive https://github.com/JoffreyVC/ethereum-pos-testnet.git
```

```bash
./build-dependencies.sh
```

## Running
Start the testnet:

```bash
./testnet.sh
```

## Configuring Prefix Lengths
Each node can be configured with a prefix length. To do this, add the --prefixlength flag to the $GETH_BINARY invocation for the node inside testnet.sh. For example:

```bash
$GETH_BINARY \
  --networkid=32382 \
  --prefixlength=24 \
  ...
```

## Main Code Changes

The most relevant changes were made in **go-ethereum**:

- `dependencies/go-ethereum/core/statedb.go`
- `dependencies/go-ethereum/core/blockchain.go`  
- `dependencies/go-ethereum/eth/protocols/eth`
- `dependencies/go-ethereum/eth/backend.go`
- `dependencies/go-ethereum/cmd/geth` 
- `dependencies/go-ethereum/kademlia` (new)  
- `dependencies/go-ethereum/partial-storage` (new)  



