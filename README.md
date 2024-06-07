# MyClothingline Token

# Overview

MyClothingline Token is an ERC20-compatible token contract deployed on the Ethereum blockchain. It facilitates the creation, transfer, and redemption of tokens, which can be used to purchase items from a clothing line.

# Functions

totalSupply: Returns the total supply of tokens.
balanceOf: Returns the token balance of a given address.
transfer: Transfers tokens from the sender to a specified recipient.
allowance: Returns the amount of tokens that an owner has approved for a spender.
approve: Approves a spender to spend a specified amount of tokens on behalf of the owner.
transferFrom: Transfers tokens on behalf of the owner to a specified recipient.
mint: Mints new tokens and adds them to the specified account.
redeem: Redeems an item from the clothing line by transferring tokens from the sender to the contract owner and marking the item as unavailable.
burn: Burns tokens, removing them from the total supply.
getAvailableItems: Returns an array of available items that can be redeemed.
getRedeemedItems: Returns an array of items that have been redeemed by a specific account.

# Owner

Casidsid, Eduard A.

# License

This project is licensed under the MIT License. See the LICENSE file for details.
