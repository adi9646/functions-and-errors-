# SimpleWallet

## Description

SimpleWallet is a basic Ethereum smart contract that allows users to deposit, withdraw, and transfer funds. It includes owner-controlled functionality to reset all balances and uses `require()`, `assert()`, and `revert()` statements to ensure the correctness and safety of operations.

## Features

- Deposit funds into the wallet.
- Withdraw funds from the wallet.
- Transfer funds to another account.
- Owner can reset all balances to zero.
- Uses Solidity's `require()`, `assert()`, and `revert()` statements for error handling.

## Requirements

### Constructor

#### `constructor()`
- Initializes the contract by setting the deployer as the owner.

### Functions

#### `deposit()`
- Allows users to deposit funds into their wallet.
- Emits a `Deposit` event.

#### `withdraw(uint256 amount)`
- Allows users to withdraw funds from their wallet.
- Requires that the withdrawal amount is greater than zero and that the user has sufficient balance.
- Emits a `Withdraw` event.

#### `transfer(address to, uint256 amount)`
- Allows users to transfer funds to another account.
- Requires a valid recipient address, a transfer amount greater than zero, and that the sender has sufficient balance.
- Emits a `Transfer` event.

#### `resetWallet()`
- Allows the owner to reset all balances to zero.
- Uses a loop to iterate through possible addresses (illustrative only; not feasible in practice).
- Reverts the transaction if no balances are found to reset.

## Error Handling

- `require()`: Ensures conditions such as non-zero amounts and sufficient balances before proceeding with transactions.
- `assert()`: Used to verify the correctness of internal state changes.
- `revert()`: Used in the `resetWallet` function to revert the transaction if no balances are found to reset.

## Events

- `Deposit(address indexed account, uint256 amount)`: Emitted when a deposit is made.
- `Withdraw(address indexed account, uint256 amount)`: Emitted when a withdrawal is made.
- `Transfer(address indexed from, address indexed to, uint256 amount)`: Emitted when a transfer is made.

# Help

For any issues, you can refer to the Remix documentation or common Ethereum development resources.

# Author
Adhamya sanotch

[@22BCS15122] (adhi9646@gmail.com)

# license

This project is licensed under the MIT License - see the LICENSE.md file for details

