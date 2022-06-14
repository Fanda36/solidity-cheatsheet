# Solidity cheatsheet

Solidity is the programing language to write smart contracts. The code is compilated to bytecode and it's run in Ethereum Virtual Machine (EVM). A blockchain is a state and it's possible to modify a state by a smart contract.

## Cheatsheets
- https://docs.soliditylang.org/en/v0.8.14/cheatsheet.html
- https://solidity-by-example.org/

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
