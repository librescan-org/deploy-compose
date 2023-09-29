# deploy-compose

Sample manifest file for deploying LibreScan with Docker Compose.

The deployment depends on an external RPC endpoint which is exposed from an OpenEthereum compatible archive node.

LibreScan works with any OpenEthereum derivative blockchain node, which exposes the trace_* RPC namespace in a compatible manner.
The node exposing the RPC endpoint must be running in full-archive mode. This can be a self-hosted node as well of course.

Some example node providers are:

- [QuickNode](https://www.quicknode.com?tap_a=67226-09396e&tap_s=4155448-b52731&utm_source=affiliate&utm_campaign=generic&utm_content=affiliate_landing_page&utm_medium=generic)
- [LlamaNodes](https://llamarpc.com/eth)
- [Alchemy](https://alchemy.com)
- [Infura](https://infura.io)

## Deployment step-by-step

### 1.) Obtain an RPC endpoint

LibreScan scrapes data off an RPC endpoint as described above.
This RPC endpoint needs to be passed as an ENV variable to the scraper service.
Once you have obtained your RPC endpoint URL (either from your own node or from a provider) replace the default one in the ```docker-compose.yml``` file.

### 2.) Launch the configured compose stack

Just run ```docker compose up -d```.
If you want to observe the logs of the underlying services, execute ```docker compose logs -f``` afterwards.

### 3.) Open the web based frontend

The web interface will be made available at [http://localhost:3000](http://localhost:3000) by default.

### 4.) Wait for sync and scraping to finish

If you are starting to sync a brand new instance, this will take days. This is not a LibreScan limitation, but generally blockchain sync time takes this much.
Afterwards you will be kept up to date, and even relaunching after a couple weeks being offline will resync super quickly.


