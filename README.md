# Fabric Chaincode dev-mode environment

Normally chaincode is started and maintained by Peer. However in “dev” mode, chaincode is built and started by the user.

This project has been created especially for rapid code/build/run/debug cycle of [tracking-project](https://github.com/intelipost/blockchain-chaincode-tracking-code) chaincode. However you can easily incorporate it with other chaincodes.

## Prerequisites
You need to have Hyperledger Fabric 1.4.0 installed ([available at this link](https://hyperledger-fabric.readthedocs.io/en/release-1.4/install.html#install-samples-binaries-and-docker-images))

## Installation
```bash
git clone https://github.com/Jojoooo1/dev-mode-environment
cd dev-mode-environment/chaincode
git clone https://github.com/intelipost/blockchain-chaincode-tracking-code
cd blockchain-chaincode-tracking-code && npm install && npm run build
cd ../../
```

## Use
For avoiding containers collisions you can remove all your running containers:
```bash
./reset.sh
```
Then start the project:

```bash
./start.sh
```

It will start your chaincode container in another terminal and invoke the function `solicitarCodigo`. If you want to try the other functions:

-  Copy one tracking code from the chaincode container logs
-  Open `start.sh` and look for the two commented functions at the end
-  Replace the tracking code with the one copied earlier
-  Run it in your terminal
