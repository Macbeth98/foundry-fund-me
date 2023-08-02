# Foundry Fund me

## Description

This is a simple Fund the owner contract that accepts ETH from users and the funds can only be withdrawn by the owner. The contract accepts a deposit value of at least 5 USD and for this the contract has Aggregator price feed contract from where it is pulling the ETH/USD conversion.

## Scripts

The Script folder contains the script to deploy the contract and the script for integration testing.

## Testing

The contract `FundMe` has been properly tested. Check the test folder for more information.

## Commands

- To compile or build the contracts. Use:
  `forge compile`
  Or `forge build`

- To run a script.
  `forge script script/scriptFileName.sol`

  - To Deploy the contract use script
    `forge script script/DeployFundMe.sol`

- To test the contracts
  `forge test`

  - To run a specific test
    `forge test --match-test testFunctionName`
  - To run the test on a chain
    `forge test --fork-url <<RPC_URL>>`
  - To get the coverage of Test.
    `forge coverage`
  - The coverage can also be run against the fork.
    `forge coverage --fork-rul <<RPC_URL>>`

- To Deploy the contract on a chain and verify the contracts
  `forge script script/DeployFundMe.s.sol:DeployFundMe --rpc-url $(SEPOLIA_RPC_URL) --private-key $(PRIVATE_KEY) --broadcast --verify --etherscan-api-key $(ETHERSCAN_API_KEY) -vvvv`
