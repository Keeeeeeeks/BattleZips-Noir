# ZK-Battleship

[![License: CC BY-SA 4.0](https://img.shields.io/badge/License-CC%20BY--SA%204.0-lightgrey.svg)](https://creativecommons.org/licenses/by-sa/4.0/)

This fork of `zkbattleship-circuit` uses a zkSNARK arithmetic circuit implementation by [tommymsz006](https://github.com/tommymsz006/zkbattleship), a prototype [Battleship](https://en.wikipedia.org/wiki/Battleship_(game)) game built on zkSNARKs proof and verification. It is being updated for 2022 and work is in progress.

## Steps to run and install demo (requires Unix)
0. [Ensure circom is installed locally](https://web.archive.org/web/20211104133455/https://docs.circom.io/getting-started/installation/)
1. run POT15 ceremony (⏰ expected 10 minute run time ⏰)
```
yarn ptau
```
2. Build zkeys and verification keys for each circuit, then export to Solidity contract (⌛ expected 3 minute run time ⌛)
```
yarn setup
```
3. Test local demonstration of full battleship game driven by ZK-Snarks
```
yarn hardhat test
```
4. Add mnemonic, infura key to .env (see .example.env as well)
```
MNEMONIC=word1 word2 word3 word4 word5 word6 word7 word8 word9 word10 word11 word12
INFURA=xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx
```
Ensure first 3 accounts are funded to deploy/ interact with contracts
5. Test on-chain demonstration of full battleship game driven by ZK-Snarks (example goerli)
```
yarn hardhat test --network goerli
```
