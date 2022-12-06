# Intro to Ethereum
# Intro to Ether
## What is a cryptocurrency?
**A cryptocurrency is a medium of exchange secured by a blockchain-based ledger**
- Medium of exchange: anything could use to exchange for goods and services
- Ledger: data store keeps track of transaction
- Blockchain technology allowed store ledger without reliance on a trusted third party.

## What is ETHER?
**ETHER is the native cryptocurrency of Ethereum**
- Payment for gas (transaction fees)
- Deposit to become a validator
- Collateral in DeFi
- Payment 

Ethereum is a computer which developers share a pool of finite computing power. **Gas fees depend** on the computing power required to execute transaction *and/or* demand for computing power at the time.
- Prevent malicious loop (run out of Ether)

## Minting Ether
**New Ether is created on Ethereum ledger**
- Ether is minted as a reward for each block proposed (issuance)
- Amount depends on the number of validators and ether they have staked.
    - Block proposer: 1/8 of issuance + tips from txn fees (recycle ether)
    - Remainder: distributed accross the other validators

## Burning
**Ether get destroyed in every txn**
- Base gas fees get destroyed
- Ether can be burned more that minted

## Denominations of ether
Denomination | Value in ether | Common usage
---|---|---
Wei|10<sup>-18 | Technical implementations
Gwei (giga-wei) | 10<sup>-9 | Human-readable gas fees

## Transfering Ether
`value`
- Transfer from account to account
- Transfer from account to smart contract (gas)

## Querying ether
`balance`

# Introduction to dapps
> **Decentralized application is an application built on blockchain with a smart contract and a UI**

## Definition of a dapp
**Backend code running on a decentralized p2p network**

- Have Frontend code and UI to make calls to its backend.
- Frontend code can get hosted on decentralized storage (IPFS)


**Character:**
- Decentralized
- Deterministric (same inputs -> same outputs)
- Turing complete 
- Isolated (code executed in EVM, separate from the network)

**Smart contracts**
- Dapp's backend
- Run as programmed
- Once deployed on network -> can't change

## Benefits of Dapp development
- Zero downtime (DDOS prevented)
- Privacy (potect real-life identity)
- Resistance to censorship (everyone could use without any restriction)
- Complete data integrity (no one can change data or force a txn)
- Trustless computation/verifiable behavior (no need to trust a centralized center)

## Drawbacks of Dapp development
- Maintenance
- Performance overhead (not cheap)
- Network congestion (only 10-15 txn/sec)
- User experience
- Centralization


# Web2 vs Web3
## [Web3 benefit](#benefits-of-dapp-development)
- Payment uses native token

## [Web3 limitations](#drawbacks-of-dapp-development)
## [Centralization vs decentralization](https://ethereum.org/en/developers/docs/web2-vs-web3/)

# Accounts
**An entity with an ether balance that can send txns on Ethereum.**

## Account types
**Two types:**
- Externally-owned account (EOA) - controlled by anyone with the private keys
- Contract account - controlled by code

**Ability**
- Receive, hold and send ETH/tokens
- Interact with deployed smart contracts

### Key differences
EOA|Contract
---|---
Costs nothing to create|Using network storage -> cost gas
Can initiate txn|Can only initiate when called
Txn can only be ETH/token|Txn trigger code -> perform many kind of actions
Made up of cryptographic pair of keys|Controlled by the logic of SM code

## An account examined
**Four fields:**
- **nonce** number of txn sent/number of contract created -> prevent double spending
- **balance**
- **codeHash** hash of code of account on EVM, cannot be change, executed when account is called
- **storageRoot** 256-bit hash of the root node of a Merkle Patricia trie that encodes storage contents

## EOA and Key pairs
Create txn request (message) + sign by private key -> signature + message -> recover to verify public key

## Account creation
- **Private key** 64 hex characters
- **Public key** generated from privat key with Elliptic Curve Digital Signature Algorithm
- **Public address** 0x + last 20 bytes of Keccak-256 hash of public key

## Contract accounts
**42 hex characters**

## Validator keys
**To identify validators**

## Wallets
**An account is not a wallet**
- Wallet is UI/Application to interact with account

# Transactions
## What's a transaction
**Cryptographically signed instructions from account -> Change of state of EVM**

Information:
- `recipient` receiving address
- `signature` sender's private key signs the txn
- `nonce` 
- `value`
- `data`
- `gasLimit` maximum gas
- `maxPriorityFeePerGas` tip to validator
- `maxFeePerGas` 

### The data field
When 