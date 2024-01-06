# Gold Token (GT) Smart Contract

## Overview

This Solidity smart contract represents the Gold Token (GT), an ERC-20 token deployed on the Ethereum blockchain. The contract extends the functionality provided by the OpenZeppelin ERC20 implementation. The primary features include minting, burning, and transferring tokens. Additionally, there are specific functions, such as freezing the contract and changing the developer address, that are restricted to the developer for enhanced security.

## Smart Contract Details

### Token Information

- **Name:** Gold Token
- **Symbol:** GT
- **Decimals:** 18

### Developer

- **Address:** [Developer Address]
- **Modifier:** onlydevoleper

### State Variables

- `devoleper`: The address of the developer who has special privileges.
- `isAlive`: A boolean flag indicating whether the contract is active or frozen.

### Modifiers

- `onlydevoleper`: Ensures that only the developer can execute certain functions.

### Constructor

Upon deployment, the constructor initializes the token with an initial supply of 10 tokens, all allocated to the developer.

### Functions

1. **Minting Tokens:**
   - **Function:** `mint(address lead, uint256 bulk)`
   - **Access:** onlydevoleper
   - **Purpose:** Allows the developer to mint additional tokens and allocate them to a specified address.

2. **Burning Tokens:**
   - **Function:** `burn(uint256 bulk)`
   - **Access:** Any address
   - **Purpose:** Enables any token holder to burn a specified amount of their own tokens.

3. **Transferring Tokens:**
   - **Function:** `transferTokens(address lead, uint256 bulk)`
   - **Access:** Any address
   - **Purpose:** Allows any token holder to transfer tokens to another address.

4. **Freezing the Contract:**
   - **Function:** `freezeContract()`
   - **Access:** onlydevoleper
   - **Purpose:** Permits the developer to freeze the contract, preventing any further changes.

5. **Changing Developer Address:**
   - **Function:** `changeCreater(address newCreater)`
   - **Access:** onlydevoleper
   - **Purpose:** Enables the developer to change the address assigned as the developer.

## Usage

1. **Deployment:**
   - Deploy the contract to the Ethereum blockchain, specifying the initial parameters.

2. **Developer Privileges:**
   - Only the developer can execute functions restricted by the `onlydevoleper` modifier.

3. **Minting and Burning:**
   - Users can mint new tokens by calling the `mint` function.
   - Any token holder can burn their own tokens using the `burn` function.

4. **Transferring Tokens:**
   - Token holders can transfer tokens to other addresses using the `transferTokens` function.

5. **Freezing the Contract:**
   - The developer can freeze the contract by calling the `freezeContract` function, preventing further modifications.

6. **Changing Developer Address:**
   - The developer can change the developer address using the `changeCreater` function.

## Author

ankushsingharoy6@gmail.com
