# Design Patterns

Here are the design patterns that I have implemented in the smart contracts:

 - [Inheritance and Interfaces](#inheritance-and-interfaces)
 - [Access-Control Design Pattern](#access-control-design-pattern)

For the implementation of these design patterns, OpenZepplin's [OpenZeppelin Solidity](https://github.com/OpenZeppelin/openzeppelin-solidity) libraries were used

## Smart Contracts
This project consists of two smart contracts:

 1. [Marketplace.sol](https://github.com/miield/ConsenSys-Academy-bootcamp-2021-Final-Project/blob/master/contracts/Marketplace.sol)
 2. [Store.sol](https://github.com/miield/ConsenSys-Academy-bootcamp-2021-Final-Project/blob/master/contracts/Store.sol)

The Marketplace smart contract contains the state of admins, store owners, and the number of stores a store owner has. The Store smart contract contains the store's properties and manages the store's items. When a user wants to open a store, she/he can do it by making a call to the `addStore` function in the Marketplace contract. If successful, then the Marketplace contract is made to deploy the Store contract address.

## Inheritance and Interfaces
I have imported and inherited the Openzeppelin contracts Ownable.sol and Pausable.sol to implement their functions in the Marketplace.sol.

## Access-Control Design Pattern
Because the Marketplace contract contains two special types of users (admins and store owners), there are mappings and modifiers in place to verify that certain functions can only be executed by these users.

I have also used OpenZepplin's [Ownable](https://github.com/OpenZeppelin/openzeppelin-solidity/blob/master/contracts/ownership/Ownable.sol) smart contract in order to manage the owner of the marketplace contract, which is the address that deploys the Marketplace contract, and the owner of a store, which is the address of the user who opens a store.


