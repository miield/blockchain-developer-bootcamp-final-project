[![built-with openzeppelin](https://img.shields.io/badge/built%20with-OpenZeppelin-3677FF)](https://docs.openzeppelin.com/)

# Online Marketplace DApp

An Online Marketplace that operates on the blockchain.
Final Project for the ConsenSys Academy 2019 Developer Bootcamp

The central marketplace is managed by a group of administrators. Admins allow store owners to add stores to the marketplace. Store owners can manage their store’s inventory and funds. Shoppers can visit stores and purchase goods that are in stock using cryptocurrency.

The address that deploys the marketplace contract will be the owner of the marketplace. The owner has the same abilities as admins, but are able to delete admins and execute the emergency stop function. 

## User Stories:

An administrator opens the web app. The web app reads the address and identifies that the user is an admin, showing them admin only functions, such as managing store owners. An admin adds an address to the list of approved store owners, so if the owner of that address logs into the app, they have access to the store owner functions.

An approved store owner logs into the app. The web app recognizes their address and identifies them as a store owner. They are shown the store owner functions. They can create a new storefront that will be displayed on the marketplace. They can also see the storefronts that they have already created. They can click on a storefront to manage it. They can add/remove products to the storefront or change any of the products’ prices. They can also withdraw any funds that the store has collected from sales.

A shopper logs into the app. The web app does not recognize their address so they are shown the generic shopper application. From the main page they can browse all of the storefronts that have been created in the marketplace. Clicking on a storefront will take them to a product page. They can see a list of products offered by the store, including their price and quantity. Shoppers can purchase a product, which will debit their account and send it to the store. The quantity of the item in the store’s inventory will be reduced by the appropriate amount.

## Documentation 

Refer to:
[Avoiding Common Attacks](https://github.com/miield/ConsenSys-Academy-bootcamp-2021-Final-Project/blob/master/avoiding_common_attacks.md) 
and
[Design Pattern Decisions](https://github.com/miield/ConsenSys-Academy-bootcamp-2021-Final-Project/blob/master/design_pattern_desicions.md)

## Getting Started


### Prerequisites

What things you need to install the software and how to install them

    npm install -g ganache-cli
    npm install -g truffle

### Installing

Clone the repo:

    git clone https://github.com/miield/blockchain-developer-bootcamp-final-project.git

Install dependencies:

    npm install

Run the server:

    npm start

It will open http://localhost:3000/

### Deploying the smart contract
Run ganache to emulate an ethereum node:

    npm ganache-cli

Compile the contracts with truffle

    truffle compile

Migrate the contracts

    truffle migrate

### Configuring MetaMask
To configure MetaMask please import the mnemonic that was generated from ganache-cli.

You will also need to change the network so that it is pointing to `localhost:8545` instead of pointing to the test or main nets.

### Testing
The tests that cover the solidity smart contracts are located at `./test`. To run the tests, simply run `truffle test`.

There are 5 tests each for the `Marketplace.sol` and `Store.sol` contracts.

**Note**: ganache-cli will need to be running in order for the tests to run


## Rinkeby Deployment

Marketplace Contract Address: `0x744d9ce7b1E18C7903D1636c326CB760c7E9A3c6`

Ehterscan transaction: https://rinkeby.etherscan.io/tx/0xfefde8dc96cb99d57fa3f7b8195784ffba286b1f655d4e2e0ff14e7666a8e1c7


