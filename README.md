# VotingSystem

## Description

VotingSystem is a basic Ethereum smart contract that allows users to propose candidates, vote for candidates, and enables the owner to reset the voting system. It uses `require()`, `assert()`, and `revert()` statements to ensure the correctness and safety of operations.

## Features

- Propose candidates.
- Vote for candidates.
- Owner can end voting.
- Owner can reset the voting system.
- Uses Solidity's `require()`, `assert()`, and `revert()` statements for error handling.

# Requirements

## Smart Contract

### Constructor

#### `constructor()`
- Initializes the contract by setting the deployer as the owner and sets voting as active.

### Functions

#### `proposeCandidate(string memory name)`
- Allows the owner to propose a new candidate.
- Requires that the candidate name is not empty.
- Emits a `CandidateProposed` event.

#### `vote(uint256 candidateId)`
- Allows users to vote for a candidate.
- Requires that the user has not already voted and the candidate ID is valid.
- Emits a `VoteCast` event.

#### `endVoting()`
- Allows the owner to end the voting process.

#### `resetVoting()`
- Allows the owner to reset the voting system if voting has ended.
- Reverts the transaction if attempted during active voting.

## Error Handling

- `require()`: Ensures conditions such as non-empty candidate names, valid candidate IDs, and that users have not voted multiple times.
- `assert()`: Used to verify the correctness of internal state changes.
- `revert()`: Used in the `resetVoting` function to revert the transaction if voting is still active.

## Events

- `CandidateProposed(uint256 id, string name)`: Emitted when a candidate is proposed.
- `VoteCast(uint256 candidateId, address voter)`: Emitted when a vote is cast.


# Help

For any issues, you can refer to the Remix documentation or common Ethereum development resources.

# Author
Adhamya sanotch

[@22BCS15122] (adhi9646@gmail.com)

# license

This project is licensed under the MIT License - see the LICENSE.md file for details

