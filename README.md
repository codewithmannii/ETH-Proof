# ETH-Proof
# MyToken

MyToken is an Ethereum-based ERC20 token contract with minting and burning functionalities. This token allows the creation and destruction of tokens, enabling flexible control over the total supply.

## Project Requirements

### Contract Features

1. *Public Variables*
   - name: The name of the token (e.g., "MyToken").
   - symbol: The token abbreviation or symbol (e.g., "MTK").
   - totalSupply: The total supply of tokens.

2. *Mapping of Addresses to Balances*
   - balances: A mapping that keeps track of the balance of each address.

3. *Mint Function*
   - mint(address _to, uint256 _amount): Increases the total supply by _amount and adds _amount to the balance of _to.

4. *Burn Function*
   - burn(address _from, uint256 _amount): Decreases the total supply by _amount and subtracts _amount from the balance of _from.
   - Includes a check to ensure _from has a balance greater than or equal to _amount.

## Getting Started

These instructions will help you deploy and interact with the MyToken contract.

### Prerequisites

- *Ethereum Wallet*: An Ethereum wallet like MetaMask.
- *Remix IDE*: A web-based IDE for Solidity development.
- *Test Network*: An Ethereum test network (e.g., Ropsten, Rinkeby, or a local Ganache instance).

### Deployment

1. Open [Remix IDE](https://remix.ethereum.org/).
2. Create a new file named MyToken.sol and paste the contract code into the file.
3. Compile the contract:
   - Go to the "Solidity Compiler" tab.
   - Select the Solidity version 0.8.18.
   - Click on "Compile MyToken.sol".
4. Deploy the contract:
   - Go to the "Deploy & Run Transactions" tab.
   - Select "Injected Web3" if using MetaMask or "JavaScript VM" for a local environment.
   - Ensure you are connected to a network with sufficient funds.
   - Enter the constructor parameters: name, symbol, and totalSupply.
   - Click "Deploy".

### Interacting with the Contract

After deployment, you can interact with the contract functions:

1. *Check Balance*
   - Use the balances mapping with an address to check the token balance.
   - Example: balances[address].

2. *Mint Tokens*
   - Call the mint function to create new tokens.
   - Parameters: _to (recipient address), _amount (number of tokens to mint).
   - Example: mint("0xRecipientAddress", 100).

3. *Burn Tokens*
   - Call the burn function to destroy tokens.
   - Parameters: _from (address to burn tokens from), _amount (number of tokens to burn).
   - Example: burn("0xFromAddress", 50).

## Example Usage

### Deploying the Contract

- *Token Name*: "MyToken"
- *Token Symbol*: "MTK"
- *Total Supply*: 1000

Deploy the contract with the above parameters. The total supply of 1000 tokens will be assigned to the deployer's address.

### Minting Tokens

To mint 100 additional tokens to another address:

```solidity
mint("0xRecipientAddress", 100);
