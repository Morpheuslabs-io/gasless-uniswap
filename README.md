# gasless-uniswap
swap away without hodling ETH

===================

Morpheus Labs forked this source code from https://github.com/yashnaman/gasless-uniswap as a reference source for `gasless UniSwap` demo. Users can explore, modify and test the protocol on Morpheus Labs SEED platform.

Since this is `ISC License`, for SEED platform users or any users who need to fork or clone this source code need to explicitly fork from this repo.

===================

# Contracts

## Installation

`npm install`

## Compile, deploy and init contracts on Ropsten

  - Create a file `.secret` containing the private key of some Ropsten account

  - Run this cmd: `truffle migrate --network ropsten`

  - Set the deployed contract addresses (printed from the above step) in the file `src/js/config.js`
# Frontend UI

1. go to src directory
2. npm install
3. npm run dev

# How to test SWAP

1. Open frontend `http://0.0.0.0:9090/`

2. Ensure Metamask connected to Ropsten

3. Click `connect wallet`

4. For the `You want to swap` part, ensure that the currently-connected Metamask acccount has some tokens of the selected one.
Can use the deploying account that has run the `truffle migrate` cmd to send some tokens to

5. For the `For` part, can select any target token to be swapped with

6. For the `send swapped tokens to`, enter any address or can even use the current Metamask one

7. Ensure to click `unlock token` to `permit` the source token (at the `You want to swap` part) to be sent out for swap

8. Click `swap` and check if the entered address receives the tokens or not