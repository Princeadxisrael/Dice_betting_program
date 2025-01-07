# Dice Betting Program

This repository contains a decentralized dice betting program implemented using Rust for the Solana blockchain. The program enables users to place bets and win payouts based on the outcomes of simulated dice rolls.

## Table of Contents
- [Overview](#overview)
- [Features](#features)
- [Directory Structure](#directory-structure)
- [Installation](#installation)
- [Usage](#usage)
- [Program Instructions](#program-instructions)
- [Error Handling](#error-handling)
- [Contributing](#contributing)
- [License](#license)

## Overview
The Dice Betting Program is a smart contract that runs on the Solana blockchain. It allows users to place bets on dice rolls and win payouts if their predictions match the outcomes. The program ensures fairness and transparency, leveraging blockchain technology to handle bets, payouts, and state management securely.

## Features
- **Bet Placement**: Users can place bets with specified amounts and predictions.
- **Random Dice Rolls**: Simulated dice rolls determine the outcomes.
- **Fair Payouts**: Winnings are calculated and distributed based on predefined rules.
- **State Management**: All program states are securely stored on-chain.

## Directory Structure
programs/dice_program/src/

├── instructions/
│   ├── bet.rs          
│   ├── initialize.rs   
│   ├── mod.rs         
├── state/
│   └── bet.rs          
├── errors.rs            
├── lib.rs               

### Key Components
- **`lib.rs`**: Entry point for the program, organizing modules and defining program logic.
- **`instructions/`**: Implements specific program instructions, including initialization and betting logic.
- **`state/`**: Defines state structures used by the program.
- **`errors.rs`**: Handles error definitions to provide informative feedback.

## Installation
1. Clone the repository:
   ```bash
   git clone https://github.com/Princeadxisrael/Dice_betting_program.git
   cd Dice_betting_program/programs/dice_program

2. Install the Rust toolchain:
   ```bash
   curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh
   rustup install stable
   rustup default stable
3. Install Solana CLI tools:
   ```bash
   sh -c "$(curl -sSfL https://release.solana.com/stable/install)"
4. Build the program:
   ```bash
   cargo build-bpf

Usage

Deploy the program to the Solana blockchain:
```bash
   solana program deploy ./target/deploy/dice_program.so
```

Use the program with a frontend or CLI to interact with its features, such as placing bets and rolling dice.

Program Instructions

### 1. Initialize

Sets up the program’s state, including:

- Initializing the betting pool.

- Setting program parameters.

### 2. Bet

Allows a user to place a bet by specifying:

- Bet amount.

- Prediction for the dice roll outcome.

### Instruction Files

- initialize.rs: Handles initialization logic.

- bet.rs: Implements betting logic.

## Error Handling

The program uses custom error definitions in errors.rs to provide meaningful feedback when issues arise. Common errors include:

- Invalid bet amounts.

- Unauthorized actions.

- Incorrect program state transitions.

## Contributing

Contributions are welcome! To contribute:

1. Fork the repository.

2. Create a feature branch.

3. Commit your changes.

4. Submit a pull request.

## License

This project is licensed under the MIT License. See the LICENSE file for details.

Feel free to reach out with questions, feedback, or issues regarding the Dice Betting Program. Happy betting!
