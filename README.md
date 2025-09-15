
# 📚 ANAXIS SIH

A Minimal Tokenised Library Management System

---

## Overview

*ANAXIS SIH* is a prototype that demonstrates how libraries can use blockchain technology to manage books and publications.
Each book is represented as an NFT on the blockchain, while its metadata (title, author, barcode/ISBN) is stored on IPFS via [Web3.Storage](https://web3.storage).
The system allows librarians and users to *mint, **borrow, and **return* books through a simple web interface.

---

## Features

* 📌 *Tokenisation*: Books are minted as ERC-721 tokens.
* 🗄️ *Decentralised Storage*: Book metadata is stored on IPFS.
* 🔗 *On-chain Borrowing*: All borrow/return actions are recorded on the blockchain.
* 💻 *Lightweight Stack*: Simple Node.js backend and React frontend for quick deployment.

---

## Architecture


ANAXIS-sih/
├── contracts/          # Solidity smart contracts
│   └── BookToken.sol
│
├── backend/            # Node.js + Express API
│   ├── server.js
│   ├── package.json
│   └── .env.example
│
├── frontend/           # React dApp
│   ├── src/
│   │   ├── App.jsx
│   │   └── BookTokenABI.json
│   ├── package.json
│   └── public/index.html
│
├── README.md
└── .gitignore


---

## Getting Started

### 1️⃣ Clone the Repository

bash
git clone https://github.com/<your-username>/ANAXIS-sih.git
cd ANAXIS-sih


### 2️⃣ Install Dependencies

*Backend:*

bash
cd backend
npm install


*Frontend:*

bash
cd ../frontend
npm install


### 3️⃣ Deploy the Smart Contract

1. Open contracts/BookToken.sol in [Remix IDE](https://remix.ethereum.org).
2. Compile and deploy to an EVM testnet (e.g., Polygon Mumbai).
3. Copy the deployed contract address.

### 4️⃣ Configure Environment Variables

Create a .env file in the backend:

bash
WEB3_STORAGE_KEY=<web3_storage_api_key>
RPC_URL=https://rpc-mumbai.maticvigil.com
PRIVATE_KEY=<test_wallet_private_key>
CONTRACT_ADDR=<deployed_contract_address>


Update the same contract address in frontend/src/App.jsx (const CONTRACT).

### 5️⃣ Start Services

*Backend:*

bash
cd backend
npm start


Runs at: [http://localhost:4000](http://localhost:4000)

*Frontend:*

bash
cd ../frontend
npm start


Opens: [http://localhost:3000](http://localhost:3000)

---

## Usage

1. Enter a *barcode or ISBN* and click *Mint Book* to create an NFT.
2. Use the *Token ID* field to *Borrow* or *Return* the book.
3. All actions are recorded on-chain for transparency.

---

## Technology Stack

| Layer            | Technology               |
| ---------------- | ------------------------ |
| Smart Contract   | Solidity, OpenZeppelin   |
| Blockchain       | Polygon Mumbai (testnet) |
| Metadata Storage | IPFS via Web3.Storage    |
| Backend API      | Node.js + Express        |
| Frontend         | React + Ethers.js        |

---

## Roadmap

* 🔍 Barcode scanner integration
* 📈 Analytics for popular books & usage
* 🤝 Inter-library sharing
* 💰 Royalty model for authors/publishers

---

## License

MIT © 2025 — ANAXIS SIH Team
