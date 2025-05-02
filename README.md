# api-772

Build process
When you build the project, the following happens:

The MetaMask-specific API specs openrpc.yaml are loaded from the local file system.
The Ethereum Execution API specs are fetched from a remote URL and methods not supported/implemented by MetaMask are filtered out.
The local MetaMask specs are merged with the Ethereum specs.
Each Ethereum method is tagged with the "Ethereum API" tag.
The merged and filtered specs are written out to temporary files:
src/build/openrpc.json
src/build/multichain-openrpc.json
These files are output to the dist folder and the src/build contents are deleted.
