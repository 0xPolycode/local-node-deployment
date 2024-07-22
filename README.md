# Klaster Local Node

To start Klaster local node, provide the configuration for the node in the docker-compose file. At least the `KEY` field
should be provided (private key) of a sufficiently funded wallet which is going to be configure as the node operator.

The node reads chain config from the `chains` folder. In the example, one chain config file is given, for the local
network, with chain id 31337. The node will read and support all the chains from the `chains` folder.

Once the key is provided, run the

```bash
docker-compose up -d
```

This command will spin up the local anvil node, as the node expects it to exist as configured in the `./chains` folder.

When the local blockchain network is up, the Klaster Node will boot up and expose endpoints at:

`http://localhost:3000/`.

To see the docs navigate to:

`http://localhost:3000/docs`.
