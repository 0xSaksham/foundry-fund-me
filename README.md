# Foundry Fund Me

## Overview
**Foundry Fund Me** is a smart contract project that allows users to fund a contract based on the ETH/USD price. This README provides essential information about setting up, testing, and deploying the project.

## Table of Contents
- [Features](#features)
- [Installation](#installation)
- [Usage](#usage)
- [Testing](#testing)
- [Deployment](#deployment)
- [Scripts](#scripts)
- [Contributing](#contributing)
- [License](#license)

## Features
- **Funding Contract**: Users can fund the contract with ETH.
- **Price Conversion**: Uses Chainlink oracles to convert ETH to USD.
- **Withdrawals**: Only the contract owner can withdraw funds.
- **Integration Tests**: Comprehensive tests for functionalities.

## Installation
To get started, clone the repository and install the necessary dependencies:

```bash
git clone <repository-url>
cd <repository-directory>
forge install
```

### Dependencies
This project uses several submodules:
- `forge-std`: Standard library for Foundry.
- `chainlink-brownie-contracts`: Chainlink contracts for price feeds.
- `foundry-devops`: Tools for deploying contracts.

## Usage
### Building the Project
To build the project, run:

```bash
forge build
```

### Formatting Code
Ensure your code is properly formatted:

```bash
forge fmt
```

## Testing
Run unit and integration tests using:

```bash
forge test -vvv
```

### Test Coverage
To check test coverage, use:

```bash
forge coverage
```

## Deployment
### Local Deployment
To deploy on a local network, use:

```bash
forge script script/DeployFundMe.s.sol:DeployFundMe --rpc-url http://localhost:8545 --private-key <your-private-key> --broadcast
```

### Deploy to Sepolia Testnet
For deployment to Sepolia:

```bash
forge script script/DeployFundMe.s.sol:DeployFundMe --network sepolia --rpc-url <sepolia-rpc-url> --account <your-account> --broadcast --verify --etherscan-api-key <your-api-key>
```

## Scripts
The project includes various scripts for interactions:
- **Funding**: `script/Interactions.s.sol` allows funding the contract.
- **Withdrawals**: The same script can be used to withdraw funds from the contract.

## Contributing
Contributions are welcome! Please follow these steps:
1. Fork the repository.
2. Create a feature branch (`git checkout -b feature/AmazingFeature`).
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`).
4. Push to the branch (`git push origin feature/AmazingFeature`).
5. Open a pull request.

## License
This project is licensed under the MIT License. See the LICENSE file for more details.
