# EtherVault

A Solidity learning game that teaches smart contract concepts through interactive challenges.

## Overview

EtherVault is an educational Lisk smart contract designed to teach Solidity programming concepts through a gamified experience. Players interact with the contract by sending Ether, solving challenges, and learning about smart contract security in a hands-on way.

## How It Works

The contract acts as a vault where users can:
1. Send Ether to become eligible for withdrawals
2. Complete challenges to increase their withdrawal limits
3. Withdraw Ether after a lock period

## Player Roles & Withdrawal Limits

Players can unlock higher withdrawal limits by progressing through different roles:

| Role | Withdrawal Limit | How to Unlock |
|------|------------------|---------------|
| Whitelisted | 0.0005 ETH | Added by contract owner |
| Magic Word | 0.001 ETH | Guess the magic word ("Solidity") |
| Big Spender | 0.003 ETH | Deposit at least 0.03 ETH |

## Game Rules

- **Lock Period**: No withdrawals allowed in the first 2 days after contract deployment
- **Withdrawal Delay**: Players must wait 1 hour between consecutive withdrawals
- **Big Spender Threshold**: Must deposit at least 0.03 ETH to qualify for the highest tier
- **Magic Word Challenge**: Players must correctly guess the magic word (hint: it's "Solidity")

## Contract Functions

### For Players

- `deposit()`: Send ETH to the contract (minimum 0.03 ETH)
- `guessMagicWord(string)`: Try to guess the magic word
- `withdraw()`: Withdraw ETH based on your role's limit
- `canWithdraw(address)`: Check if you can withdraw at the current time
- `getWithdrawalLimit(address)`: Check your current withdrawal limit
- `getVaultBalance()`: View the current ETH balance in the contract

### For Contract Owner

- `addToWhitelist(address[])`: Add multiple addresses to the whitelist
- `removeFromWhitelist(address[])`: Remove addresses from the whitelist
- `checkWhitelistStatus(address)`: Check if an address is whitelisted

## Technical Details

- **Solidity Version**: ^0.8.20
- **Lock Period**: 2 days
- **Withdrawal Delay**: 1 hour
- **Magic Word Hash**: `0xe12a28df6f8731c94ade6605c8f457c16b3f591ecc3be3d092af1f56215a3da2`
- **Contract Owner**: `0xbf4EE65FE67C291DfC34ffe2455ecA9d97DF9148`
- **Deployed Contract**: [View on Lisk Sepolia Blockscout](https://sepolia-blockscout.lisk.com/address/0x6dA826f51c447354f65A7480e5364672785C0417)

## Learning Objectives

By interacting with EtherVault, you'll learn about:

- Solidity function visibility modifiers
- Role-based access control
- Time-based constraints in smart contracts
- Handling Ether transactions
- Security best practices in smart contract development
- Hash verification techniques
- Event emission for transparency

## Getting Started

1. The contract is already deployed on Lisk Sepolia testnet
2. Send ETH to the contract via deposit
3. Try to get whitelisted or guess the magic word
4. Wait for the lock period to end
5. Withdraw ETH based on your role's limit

## Security Notes

This contract is designed for educational purposes. Some concepts demonstrated include:
- Secure withdrawal patterns
- Role-based access control
- Time locks and cooldown periods

## Additional Resources

For more details on the contract implementation and challenges:
- Visit: `https://tinyurl.com/EtherVault`
- Review the contract source code comments
- Experiment with different roles and withdrawal patterns

---

Happy learning and enjoy exploring Solidity concepts with EtherVault!
