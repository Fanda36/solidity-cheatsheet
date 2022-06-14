# Solidity cheatsheet

Solidity is the programing language to write smart contracts. The code is compilated to bytecode and it's run in Ethereum Virtual Machine (EVM). A blockchain is a state and it's possible to modify a state by a smart contract.

## Gas
- each code run needs `gas`
- **You don't need gas if you don't modify the state** - `view` and `pure` functions
  - you pay gas if you run `view` or `pure` functions inside transacion
