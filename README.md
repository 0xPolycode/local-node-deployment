# MEE Local Node

To start MEE local node, provide the configuration for the node in the docker-compose file. At least the `KEY` field
should be provided (private key) of a sufficiently funded wallet which is going to be configured as the node operator.

The node reads chain config from the mapped `chains` folder. In the example docker-compose file, chains-testnet folder is being provided to the node.

IMPORTANT: Make sure to replace <YOUR-RPC-URL> placeholder in every chain config json descriptor from the chains folder before spinning up the node. RPCs are supposed to be able to run the ```debug_traceCall``` operation - if you're using 3rd party RPCs, this is something you'd have to make sure is exposed to you by the RPC provider.

Once the funded key is provided & RPCs configured, run the

```bash
docker-compose up -d
```

The MEE Node will boot up and expose endpoints at:

`http://localhost:3000/`.

To see the docs navigate to:

`http://localhost:3000/docs`.
