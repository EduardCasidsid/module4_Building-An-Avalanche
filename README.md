# module4_Building-An-Avalanche
# MyClothing Line Contract

## Overview
MyToken is an ERC20 token contract with additional features such as minting, burning, redeeming items, and managing ownership.

## Functions

### totalSupply()
Returns the total supply of the token.

### balanceOf(address account)
Returns the balance of the specified account.

### transfer(address recipient, uint256 amount)
Transfers tokens from the sender to the recipient.

### allowance(address owner, address spender)
Returns the allowance of spender for the specified owner.

### approve(address spender, uint256 amount)
Approves the spender to spend a specified amount of tokens on behalf of the owner.

### transferFrom(address sender, address recipient, uint256 amount)
Transfers tokens from one account to another if the sender has enough allowance.

### mint(address account, uint256 amount)
Mints a specified amount of tokens and assigns them to the specified account.

### redeem(uint256 itemIndex)
Redeems an item from the contract using tokens.

### burn(uint256 amount)
Burns a specified amount of tokens, reducing the total supply.

### getAvailableItems()
Returns an array of available items that can be redeemed using tokens.

## Owner
The contract is owned by an address specified during deployment.

## License
This contract is licensed under the MIT License.
