Sure thing 😊 — here’s a clean `README.md` for your **ANAXIS SIH** project:

---

# 📚 ANAXIS SIH

> Tokenized Library Management System – built with **Solidity**, **IPFS (Web3.Storage)**, **Node.js**, and **React**.

ANAXIS SIH lets libraries register books as NFTs on-chain, store metadata on IPFS, and allow students to borrow/return books via a simple web interface.

---

## ✨ Features

* **ERC721 Smart Contract** for books
* **IPFS storage** of metadata via [Web3.Storage](https://web3.storage)
* **Backend API** (Node + Express) to upload metadata & mint NFTs
* **Frontend (React)** to mint, borrow, and return books
* Works with any EVM chain (Polygon, Sepolia, etc.)

---

## 📁 Project Structure

```
ANAXIS-sih/
├── contracts/          # Solidity smart contracts
│   └── BookToken.sol
│
├── backend/            # Node.js + Express server
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
```

---

## 🚀 Getting Started

### 1️⃣ Clone the repository

```bash
git clone https://github.com/<your-username>/ANAXIS-sih.git
cd ANAXIS-sih
```

### 2️⃣ Install dependencies

Backend:

```bash
cd backend
npm install
```

Frontend:

```bash
cd ../frontend
npm install
```

### 3️⃣ Deploy the smart contract

1. Use [Remix](https://remix.ethereum.org) or Hardhat to deploy `contracts/BookToken.sol`.
2. Copy the deployed contract address into:

   * `backend/.env` → `CONTRACT_ADDR`
   * `frontend/src/App.jsx` → `CONTRACT`

### 4️⃣ Configure environment

Create a `.env` in `backend/`:

```bash
WEB3_STORAGE_KEY=your_web3_storage_token
RPC_URL=https://rpc-mumbai.maticvigil.com
PRIVATE_KEY=your_test_wallet_private_key
CONTRACT_ADDR=your_contract_address
```

### 5️⃣ Run the backend

```bash
cd backend
npm start
# runs on http://localhost:4000
```

### 6️⃣ Run the frontend

```bash
cd frontend
npm start
# opens http://localhost:3000
```

---

## 🧪 Usage

* Enter a **barcode/ISBN** and click `Mint Book` → NFT is created.
* Enter the NFT’s **Token ID** to `Borrow` or `Return` the book.
* All borrow/return actions happen on-chain.

---

## 🛠 Tech Stack

* [Solidity](https://soliditylang.org/) – smart contracts
* [OpenZeppelin](https://openzeppelin.com/contracts/) – ERC721 helpers
* [Web3.Storage](https://web3.storage) – IPFS file hosting
* [Node.js + Express](https://expressjs.com/) – backend API
* [React](https://react.dev/) – frontend dApp
* [Ethers.js](https://docs.ethers.io/) – Ethereum interaction

---

## 📜 License

MIT © 2025 – ANAXIS SIH Team

---

Would you like me to include example screenshots or GIFs of the UI in the README as well?
