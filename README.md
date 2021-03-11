# Gasless UniSwap

This dApp enables decentralized swapping of ERC20 tokens without the need of holding ETH to pay for tx fee

Currently-supported network is Ropsten Ethereum Testnet

===================

Morpheus Labs forked this source code from https://github.com/yashnaman/gasless-uniswap as a reference source for `gasless UniSwap` demo. Users can explore, modify and test the protocol on Morpheus Labs SEED platform.

Since this is `ISC License`, for SEED platform users or any users who need to fork or clone this source code need to explicitly fork from this repo.

===================

# Smart contract

In the folder `gasless-uniswap`

## Installation

Run this cmd

`npm install`

## Compile, deploy and init contracts on Ropsten testnet of Ethereum

  - Create a file `.secret` containing the private key of some Ropsten account

  - Run this cmd: `truffle migrate --network ropsten`

  - Set the deployed contract addresses (printed from the above step) in the file `src/js/config.js` under the section `config.ropsten`

  - On the Metamask, these contract addresses should also be added by using the `Add Token`/`Custom Token`. This is to visualize the tokens and their balances on Metamask wallet.

**Notice**

The process `truffle migrate` takes long time (about 30 minutes) for contract initialization

# Frontend UI

Go to `src` directory

## Installation

Run this cmd

`npm install`

## Start the frontend

Run this cmd

`npm run dev`

Open web browser

`http://0.0.0.0:9090/`

# How to test `swap`

1. Open web browser: `http://0.0.0.0:9090/`

2. Ensure Metamask connected to **Ropsten**

3. Click `connect wallet` to get connected to Metamask

4. For the `You want to swap` part, ensure that the currently-connected Metamask acccount has some tokens of the selected token to be swapped. Can use the account (whose private key is specified in the file `.secret`) that has run the `truffle migrate` cmd to send some tokens to

5. For the `For` part, can select any target token to be swapped with

6. For the `send swapped tokens to` part, enter some address to receive the tokens

7. For the `Unlock Your Tokens` part, ensure to click `unlock token` to `permit` the source token (at the `You want to swap` part) to be sent out for swap. 

8. Click `swap` button and check if the entered address receives the tokens or not on Metamask wallet

## Test transaction result on Ropsten

1. `unlock token` or `permit` tx

https://ropsten.etherscan.io/tx/0x9282b118c0da7135beb4454afcb1b38d84cf796cb48092b0bb9fd9ce26150481

2. `swap` tx

https://ropsten.etherscan.io/tx/0x3297b1e7d05c52d5bab0fb7f32e0eb01690ba8373593049436ffe4a1a39f0a24

# How to test `Add Liquidity`

1. Open web browser: `http://0.0.0.0:9090/`

2. Ensure Metamask connected to **Ropsten**

3. Click `connect wallet` to get connected to Metamask

4. For the `You want to swap` part, ensure that the currently-connected Metamask acccount has some tokens of the selected token to be unlocked. Can use the account (whose private key is specified in the file `.secret`) that has run the `truffle migrate` cmd to send some tokens to. Then, click the button `unlock token`.

5. For the `For` part, do similarly to the step above

6. For the `send Liquidity tokens to` part, enter some address to receive the `UNI-V2` tokens

7. Click `Add Liquidity` button and check if the entered address receives the `UNI-V2` tokens or not on Metamask wallet

## Test transaction result on Ropsten

1. `unlock token` or `permit` tx for the part `You want to swap`

https://ropsten.etherscan.io/tx/0xb627558cebd2500b42b79686d266217759b7ac9aec24dc21bf4c3f9cac1e4f1d

2. `unlock token` or `permit` tx for the part `For`

https://ropsten.etherscan.io/tx/0xe69447609a00a79af844a6f29648b2b241ba8995a68a1134a56839428ed5e085

3. `Add Liquidity` tx 

https://ropsten.etherscan.io/tx/0x2874056a411d302977c521530df59fa8b247e206c3424dae33fe7f952578e6e2

