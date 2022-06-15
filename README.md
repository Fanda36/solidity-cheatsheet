# Solidity cheatsheet

Solidity is the programing language to write smart contracts. The code is compilated to bytecode and it's run in Ethereum Virtual Machine (EVM). A blockchain is a state and it's possible to modify a state by a smart contract.

## Tutorials
- https://www.youtube.com/watch?v=gyMwXuJrbJQ

## Cheatsheets
- https://docs.soliditylang.org/en/v0.8.14/cheatsheet.html
- https://solidity-by-example.org/

# Tools and frameworks
- Ethers.js (alternative Web3.js)
  - js library to interact with blockchain (creating transactions etc.)
  - https://docs.ethers.io/
- Ganache 
  - personal Ethereum blockchain node writen in Node.js
  - https://trufflesuite.com/ganache/
- Hardhat
  - development environment, includes custom blockchain node, ethers.js, testing etc.
  - https://hardhat.org/

## Gas
- each code run needs `gas`
- **You don't need gas if you don't modify the state** - `view` and `pure` functions
  - you pay gas if you run `view` or `pure` functions inside transacion
- optimalization - use `constant` and `immutable`

## modifier
```js
modifier onlyOwner {
    // require(msg.sender == owner);
    if (msg.sender != i_owner) revert NotOwner();
    _;
}
```

## library
- `using MyLibrary for uint256;`
- extend uint256 by new methods from MyLibrary
- first parameter is current value
