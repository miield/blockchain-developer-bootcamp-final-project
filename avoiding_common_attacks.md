# Avoiding Common Attacks
Smart contract security is not easy. Many attacks on smart contracts have caused millions of dollars of ether lost or stolen. However, there are best practices to follow and here are some that I have implemented in my smart contract design:

 - [Using Specific Compiler Pragma](#using-specific-compiler-pragma)
 - [Use Modifiers Only for Validation](#use-modifiers-only-for-validation)

## Using Specific Compiler Pragma
It's the best practice to lock the compiler version to the one used to test your contract to avoid any kind of issue that might be introduced in the new versions. Lets say a new compiler version introduce a vulnerability, that might affect your contract as well.


## Use Modifiers Only For Validation
In the `Marketplace` contract, there are two special types of users. One being admins, the other being store owners. Shoppers are just regular users who have an address that is not specified in neither the `admins` nor the `storeOwners` mapping.

Admins are able to create other admins and store owners, but they are not able to delete other admins. Only the user who has deployed the `Marketplace` contract is able to delete other admins. In a truly decentralized application, perhaps there would be no admins, but users would apply with a fee, to become a store owner - though there will need to be some kind of interesting governance in place to make sure the marketplace stay ethical.

Store owners are have complete of their own store - especially when it comes to the funds of the stores. They do not have the abilities that the admins have because admins functions are protected by using modifiers.

The user who deploys the `Marketplace` contract is also an admin by default, but also has access to a couple of privileges that regular admins don't get. One is the ability to delete admins. The other is the ability to execute the emergency stop for the marketplace - and all store contracts that are created by the marketplace. The emergency stop function prevents any action from happening except for allowing store owner to withdraw funds from their stores.
