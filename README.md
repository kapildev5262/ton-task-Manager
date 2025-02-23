# Task Management Smart Contract on TON Blockchain

This project is a smart contract written in FunC for the TON Blockchain. It enables users to create tasks, complete them, and claim rewards. The contract ensures fair reward distribution among participants and tracks completed tasks.

## Features
- **Task Creation**: Users can create tasks with a description, maximum participants, and reward amount.
- **Task Completion**: Only the task creator can mark a task as completed for a participant.
- **Reward Claiming**: Participants can claim their rewards after completing a task.
- **Fair Reward Distribution**: Rewards are divided equally among all participants.
- **Task Tracking**: The contract tracks completed tasks to prevent double claims.

## Code Structure
- **`contracts/task.fc`**: The main FunC smart contract.
- **`tests/Task.spec.ts`**: Jest tests for the smart contract.
- **Wrappers**: Helper files for interacting with the contract.
- **`build/task.cell`**: Compiled smart contract output.

## Prerequisites
- Node.js
- Func compiler (`func-js`)
- Jest (for testing)
- Blueprint (TON development framework)

## Installation
1. Clone the repository:
   ```bash
   git clone https://github.com/your-username/task-management-ton.git
   cd task-management-ton
   ```

1. Install dependencies:
    ```bash
    npm install
    ```

### Build

`npx blueprint build` or `yarn blueprint build`

### Test

`npx blueprint test` or `yarn blueprint test`

### Test Output Example
```
> task@0.0.1 test
> jest --verbose

 PASS  tests/Task.spec.ts (5.144 s)
  Task
    ✓ should deploy (383 ms)
    ✓ should create a task successfully (203 ms)
    ✓ should complete task only by creator (231 ms)
    ✓ should allow claiming rewards for completed tasks (258 ms)
    ✓ should divide reward equally among all participants (284 ms)

Test Suites: 1 passed, 1 total
Tests:       5 passed, 5 total
Snapshots:   0 total
Time:        5.304 s
Ran all test suites.
```
## Usage
1. Deploy the contract to the TON Blockchain.

2. Use the provided wrappers to interact with the contract:

- Create a task.

- Complete a task.

- Claim rewards.

### Deploy or run another script

`npx blueprint run` or `yarn blueprint run`

### Add a new contract

`npx blueprint create ContractName` or `yarn blueprint create ContractName`
