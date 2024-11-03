# Upgradable Smart Contracts Project

This project demonstrates the implementation of upgradable smart contracts in Solidity. It was developed as part of an advanced smart contract development course, focusing on understanding and applying proxy patterns to make contracts upgradable over time. The project consists of a basic storage contract that can be upgraded without altering its address, enabling developers to enhance functionality while maintaining a stable user interface.

**Disclaimer**: This project is intended for educational purposes only and has been thoroughly tested. It should not be deployed on mainnets.

## Index

- [Upgradable Smart Contracts Project](#upgradable-smart-contracts-project)
  - [Index](#index)
  - [Project Overview](#project-overview)
    - [Files Included](#files-included)
  - [Installation](#installation)
  - [License](#license)

## Project Overview

The project uses a proxy contract pattern to allow upgrades in the storage contract's functionality. Initially, the contract (`BoxV1.sol`) supports storing a single number, and through an upgrade, it expands its functionality to store an additional string (`BoxV2.sol`).

### Files Included

- **BoxV1.sol**: The initial version of the contract, which supports setting and getting a number.
- **BoxV2.sol**: The upgraded version of the contract that adds functionality to set and retrieve a name in addition to the number.
- **DeployBox.s.sol**: The deployment script for the initial contract version.
- **UpgradeBox.s.sol**: The script to upgrade the contract to `BoxV2`.
- **DeployAndUpgradeTest.t.sol**: A test script to verify both the initial deployment and the upgrade functionality.

## Installation

Ensure that you have the following dependencies:

- Solidity (0.8.0 or higher)
- Foundry (for testing and deployment)
- Node.js and npm (for dependency management if necessary)

Clone the repository and install dependencies:

```bash
git clone https://github.com/jumpupjoran/foundry-upgradable-contracts.git
cd foundry-upgradable-contracts
```

deploy the contract to anvil:

1. anvil

   ```bash
   make deploy
   ```

2. upgrade the contract

   ```bash
   make upgrade
   ```

3. sepolia
   ```bash
   make deploy-sepolia
   ```

## License

This project is licensed under the MIT License. See the LICENSE file for more details.
