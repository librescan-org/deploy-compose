# deploy-compose

Sample manifest file for deploying LibreScan with Docker Compose.

The deployment depends on an external RPC endpoint which is exposed from an OpenEthereum compatible archive node.

LibreScan works with any OpenEthereum derivative blockchain node, which exposes the trace_* RPC namespace in a compatible manner.
The node exposing the RPC endpoint must be running in full-archive mode.

Some example nodes are:

- [QuickNode](https://www.quicknode.com?tap_a=67226-09396e&tap_s=4155448-b52731&utm_source=affiliate&utm_campaign=generic&utm_content=affiliate_landing_page&utm_medium=generic)
- [LlamaNodes](https://llamarpc.com/eth)
- [Alchemy](https://alchemy.com)
- [Infura](https://infura.io)
