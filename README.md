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

