# Solidity Contracts README

This repository contains two Solidity smart contracts: `Vault.sol` and `ERC20.sol`. Below is an overview of each contract along with instructions on how to use them.

## Vault.sol

### Overview
`Vault.sol` is a contract that acts as a vault for storing ERC20 tokens. Users can deposit tokens into the vault and receive shares in return, which represent their ownership stake in the vault. These shares can later be redeemed for tokens when users withdraw from the vault.

### Functions
1. **constructor(address _token)**
    - Initializes the contract with the address of the ERC20 token that will be stored in the vault.

2. **deposit(uint _amount) external**
    - Allows users to deposit ERC20 tokens into the vault.
    - Calculates the number of shares to mint for the depositor based on the current total supply of shares and the amount of tokens deposited.
    - Transfers the deposited tokens from the user to the vault and mints the corresponding shares to the user.

3. **withdraw(uint _shares) external**
    - Allows users to withdraw ERC20 tokens from the vault by burning their shares.
    - Calculates the amount of tokens to redeem based on the number of shares burned and the current total supply of shares.
    - Transfers the redeemed tokens from the vault to the user and burns the corresponding shares.

### Usage
1. Deploy the `Vault` contract, providing the address of the ERC20 token to be stored.
2. Users can deposit tokens into the vault using the `deposit` function.
3. Users can withdraw tokens from the vault using the `withdraw` function.

## ERC20.sol

### Overview
`ERC20.sol` is an implementation of the ERC20 token standard. It allows for the creation of fungible tokens on the Ethereum blockchain.

### Functions
1. **mint(uint amount) external**
    - Mints new tokens and assigns them to the caller's balance.
    - Increases the total supply of tokens.

2. **burn(uint amount) external**
    - Burns tokens from the caller's balance.
    - Decreases the total supply of tokens.

3. **transfer(address recipient, uint amount) external**
    - Transfers tokens from the caller's balance to the specified recipient.

4. **approve(address spender, uint amount) external**
    - Allows the spender to withdraw tokens from the caller's account, up to the specified amount.

5. **transferFrom(address sender, address recipient, uint amount) external**
    - Transfers tokens from the sender's balance to the recipient.
    - Requires prior approval from the sender to spend tokens by the caller.

### Usage
1. Deploy the `ERC20` contract to create a new ERC20 token.
2. Users can interact with the token by calling functions such as `transfer`, `approve`, and `transferFrom` to transfer tokens between accounts.
3. The contract owner can mint new tokens using the `mint` function and burn tokens using the `burn` function.

## License
Both contracts are licensed under the MIT License.

## AUTHOR

DEEPAK RAJ
