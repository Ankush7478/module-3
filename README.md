# Token Smart Contract

## Overview

This repository contains a simple ERC-20 token smart contract implemented in Solidity. The contract extends the OpenZeppelin ERC20 implementation and includes additional functionality for minting, burning, transferring tokens, freezing the contract, and changing the contract creator.

## Smart Contract Details

### Token Details

- **Name:** Gold Token
- **Symbol:** GT

### Main Features

1. **Minting Tokens:** The contract creator can mint new tokens and assign them to a specific address.

2. **Burning Tokens:** Token holders can burn a specified amount of their own tokens.

3. **Transferring Tokens:** Token holders can transfer tokens to other addresses.

4. **Freezing the Contract:** The contract creator can freeze the contract, preventing any further modifications.

5. **Changing the Contract Creator:** The contract creator can transfer the role to a new address.

### Security

- The `onlyCreater` modifier ensures that only the contract creator can execute certain functions.

- The contract uses the OpenZeppelin ERC20 implementation, a widely used and audited standard for ERC-20 tokens.

### Usage

1. **Deployment:**
   - Deploy the contract to an Ethereum-compatible blockchain.

2. **Minting Tokens:**
   - Call the `mint` function, specifying the address to receive the tokens and the amount to mint.

3. **Burning Tokens:**
   - Call the `burn` function, specifying the amount of tokens to burn.

4. **Transferring Tokens:**
   - Call the `transferTokens` function, specifying the recipient address and the amount of tokens to transfer.

5. **Freezing the Contract:**
   - Call the `freezeContract` function to freeze the contract.

6. **Changing the Contract Creator:**
   - Call the `changeCreater` function, specifying the new contract creator address.

### Example

```javascript
// Deploy the contract
let token = await Token.deployed();

// Mint 100 tokens to address 0x123
await token.mint("0x123", 100);

// Transfer 50 tokens from the deployer to address 0x456
await token.transferTokens("0x456", 50);

// Burn 25 tokens from address 0x456
await token.burn(25);

// Freeze the contract
await token.freezeContract();

// Change the contract creator to address 0x789
await token.changeCreater("0x789");
```

## License

This smart contract is licensed under the MIT License. See the [LICENSE](./LICENSE) file for details.

## Author

ankushsingharoy6@gmail.com
