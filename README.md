# module4_Building-An-Avalanche

# ClothingLine Smart Contract

## Overview

The `ClothingLine` smart contract is an ERC20 token contract with added functionality to represent different sizes of clothes. The contract allows minting, transferring, redeeming, and burning tokens which represent different sizes of clothes. The contract is managed by an owner who has the exclusive right to mint new tokens.

## Functions

### Constructor

```solidity
constructor() ERC20("Clothes", "Size") Ownable(msg.sender) {
    Clothes[1] = 400; // Small
    Clothes[2] = 600; // Medium
    Clothes[3] = 800; // Large
    Clothes[4] = 1000; // Extra Large
}
```

The constructor initializes the ERC20 token with the name "Clothes" and the symbol "Size". It also sets the initial sizes and their respective values.

### `mint`

```solidity
function mint(address _to, uint256 _amount) public onlyOwner {
    _mint(_to, _amount);
}
```

This function allows the owner to mint new tokens and transfer them to a specified address.

### `transfersize`

```solidity
function transfersize(address _to, uint256 _amount) public {
    require(balanceOf(msg.sender) >= _amount, "Transfer Failed: Insufficient balance.");
    approve(msg.sender, _amount);
    transferFrom(msg.sender, _to, _amount);
}
```

This function allows a user to transfer a specified amount of tokens to another address, ensuring the sender has enough balance to complete the transfer.

### `sizes`

```solidity
function sizes() external pure returns (string memory) {
    string memory saleOptions = " Clothes: {1} Small (400) {2} Medium(600) {3} Large (800) {4} Extra Large (1000)";
    return saleOptions;
}
```

This function returns a string representation of the available clothing sizes and their corresponding values.

### `redeem`

```solidity
function redeem(uint256 _amount) public {
    require(Clothes[_amount] > 0, " Clothes is not enough");
    require(_amount <= 3, " Clothes is not enough.");
    require(balanceOf(msg.sender) >=  Clothes[_amount], "Redeem Failed: Insufficient balance.");
    transfer(owner(),  Clothes[_amount]);
}
```

This function allows a user to redeem their tokens for clothes, transferring the required amount to the owner.

### `burn`

```solidity
function burn(uint256 _amount) public {
    require(balanceOf(msg.sender) >= _amount, "Burn Failed: Insufficient balance.");
    approve(msg.sender, _amount);
    _burn(msg.sender, _amount);
}
```

This function allows a user to burn a specified amount of their tokens, reducing the total supply.

### `getBalance`

```solidity
function getBalance() external view returns (uint256) {
    return this.balanceOf(msg.sender);
}
```

This function returns the balance of the caller.

### `decimals`

```solidity
function decimals() override public pure returns (uint8) {
    return 0;
}
```
# Owner

Eduard Casidsid
This function overrides the `decimals` function to return 0, meaning the token is indivisible.
