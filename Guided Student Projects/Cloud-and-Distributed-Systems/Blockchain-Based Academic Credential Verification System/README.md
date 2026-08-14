# ⛓️ Blockchain-Based Academic Credential Verification System

## 📌 Project Overview

The **Blockchain-Based Academic Credential Verification System** is a decentralized platform designed to provide secure, tamper-evident, and efficient academic credential issuance and verification.

The system combines **Ethereum blockchain, Solidity smart contracts, IPFS, PostgreSQL, Node.js, Express.js, and React.js** to create a multi-layer credential verification architecture.

Academic records are maintained through PostgreSQL, certificate documents are stored using IPFS, and blockchain records provide an immutable verification layer. This architecture enables detection of modified, revoked, missing, or fraudulent credentials.

## 🎯 Objectives

- To develop a decentralized academic credential verification system.
- To prevent unauthorized modification of academic credentials.
- To provide fast and reliable credential verification.
- To use blockchain for immutable credential records.
- To use IPFS for tamper-evident certificate storage.
- To implement role-based access control for credential issuance.
- To support credential revocation.
- To provide a public verification mechanism.
- To evaluate the security, reliability, and performance of the system.

## ⚙️ Key Features

- 🎓 Academic credential issuance
- ⛓️ Ethereum blockchain integration
- 📜 Solidity smart contracts
- 📦 IPFS-based certificate storage
- 🗄️ PostgreSQL database
- 🔐 Role-based access control
- 🔎 Multi-layer credential verification
- 🚫 Credential revocation
- 🛡️ Tamper detection
- 📝 Audit logging
- 🌐 React-based user interface
- 🔌 RESTful backend API
- ⚡ Near real-time verification

## 🏗️ System Architecture

```text
                Academic Credential
                        │
                        ▼
                 React Frontend
                        │
                        ▼
                Node.js / Express
                        │
          ┌─────────────┼─────────────┐
          ▼             ▼             ▼
     PostgreSQL        IPFS        Ethereum
      Database        Storage      Blockchain
          │             │             │
          └─────────────┼─────────────┘
                        ▼
               Verification Layer
                        │
                        ▼
              Verification Result
