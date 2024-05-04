### Smart Contract-Based Insurance Platform

#### Overview
This project implements a smart contract-based insurance platform on the Ethereum blockchain. The platform allows users to propose, accept, and resolve insurance contracts for flight cancellations using TLS-N proofs. The contracts are implemented in Solidity, with some supporting libraries and utility functions written in JavaScript.

#### Languages Used
- JavaScript: 53.9%
- Solidity: 44.7%
- Other: 1.4%

#### Smart Contracts
The project consists of two main smart contracts:

1. **Insurance.sol**: This contract manages the insurance covers, including proposing, accepting, resolving contracts, and retrieving contract details.
2. **Migrations.sol**: This contract handles the deployment and migration of other contracts.

#### Smart Contract Attributes
- **InsuranceCover Struct**: Defines the attributes of an insurance cover, including proposer, cover amount, premium, flight ID, and contributors.
- **State Variables**: Tracks the insurance covers and their details.
- **Events**: Emit events for various contract state changes.
- **Modifiers**: None in this contract.
- **Functions**: Public functions for proposing, accepting, resolving, canceling, and retrieving contract details.
- **Private Functions**: Utility functions for internal contract operations.
- **Library ECMath**: Implements elliptic curve cryptography operations used for signature verification.

#### Usage
1. **Propose Insurance Cover**: Users can propose an insurance contract by providing a TLS-N proof and specifying the total cover amount.
2. **Accept Contract**: Other users can accept the proposed contract by contributing capital until the total cover amount is reached.
3. **Resolve Contract**: Upon flight cancellation, the contract automatically resolves, and funds are distributed accordingly.
4. **Cancel Insurance Contract**: Proposers can cancel the proposed contract before it's filled, and funds are refunded.

#### Dependencies
- **JsmnSolLib**: JSON parsing library for Solidity.
- **Bytesutils.sol**: Utility library for byte operations.
- **Tlsnutils.sol**: TLS-N proof verification utility.

#### Note
Ensure proper configuration and connection to an Ethereum node for contract deployment and interaction.

#### Authors
Purvika Joshi
