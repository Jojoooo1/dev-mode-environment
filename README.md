# Fabric Chaincode dev mode environment

Normally chaincodes are started and maintained by peer. However in “dev” mode, chaincode is built and started by the user. 

This project has been created especially for rapid code/build/run/debug cycle of [tracking-project](https://github.com/intelipost/blockchain-chaincode-tracking-code) chaincode. However you can easily incorporate other chaincodes.

## Prerequisites
You need to have Hyperledger Fabric 1.4.0 installed ([available at this link](https://hyperledger-fabric.readthedocs.io/en/release-1.4/install.html#install-samples-binaries-and-docker-images))

## Installation
For avoiding containers collisions you can remove all your running containers:
```bash
./reset.sh
```
Then Copy [tracking-project](https://github.com/intelipost/blockchain-chaincode-tracking-code) folder in `chaincode/` and run:

```bash
./start.sh
```

It will start your chaincode container in another terminal and invoke the function `solicitarCodigo`. If you want to try the other functions:

-  Copy one tracking code from the chaincode container logs 
-  Open `start.sh` and look for the two commented functions at the end
-  Replace the tracking code with the one copied earlier
-  Run it in your terminal
