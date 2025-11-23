🔐 Private Subscription Calibration — FHEVM dApp

A decentralized, fully homomorphic encrypted subscription calibration dApp on Ethereum (Sepolia testnet) using Zama’s FHEVM protocol.
All user preferences are encrypted → processed homomorphically on-chain → only the final subscription plan is decrypted.

⚡ Features

Submit encrypted subscription preferences (duration, budget, content type)

Smart contract computes suitable plan without revealing private data

Homomorphic comparison and selection on-chain

Reveal only the chosen plan (e.g., Basic / Standard / Premium)

Clean glassmorphism web UI with animated feedback

Built with Relayer SDK v0.2.0 and Ethers v6

🛠 Quick Start
Prerequisites

Node.js ≥ 20

npm / yarn / pnpm

MetaMask (or any Ethereum wallet with injected provider)

Installation
Clone the repository
git clone <your-repo-url>
cd private-subscription

Install dependencies
npm install

Set up environment variables
npx hardhat vars set MNEMONIC
npx hardhat vars set INFURA_API_KEY
npx hardhat vars set ETHERSCAN_API_KEY   # optional

Compile Contracts
npm run compile

Run Tests
npm run test

Deploy to Local Network
npx hardhat node
npx hardhat deploy --network localhost

Deploy to Sepolia Testnet (Zama FHEVM)
npx hardhat deploy --network sepolia
npx hardhat verify --network sepolia <CONTRACT_ADDRESS>

📁 Project Structure
private-subscription/
├── contracts/                # Smart contracts
│   └── PrivateSubscription.sol   # Main FHE-enabled contract
├── deploy/                   # Deployment scripts
├── frontend/                 # Web frontend (UI)
│   └── index.html            # Main dApp interface
├── hardhat.config.js         # Hardhat + FHEVM setup
└── package.json              # Dependencies and scripts

📜 Available Scripts
Command	Description
npm run compile	Compile smart contracts
npm run test	Run tests
npm run clean	Clean build artifacts
npm run start	Serve frontend locally
npx hardhat deploy --network sepolia	Deploy to FHEVM Sepolia testnet
npx hardhat verify	Verify deployed contract on Etherscan
🔗 Frontend Integration

The frontend uses:

Relayer SDK v0.2.0 (@zama-fhe/relayer-sdk)

Ethers.js v6 for blockchain interaction

Simple glassmorphic UI built with HTML + CSS (no framework)

Flow:

Connect wallet via MetaMask

Submit encrypted preferences (Duration, Budget, Content Type)

Smart contract computes encrypted plan handle

Owner makes plan publicly decryptable

Decrypt plan with Relayer SDK → display result (“Basic”, “Standard”, “Premium”)

📚 Documentation

Zama FHEVM Docs

Solidity Guide — FHE Operations

Relayer SDK Guide

Ethers v6 Documentation

🆘 Support

🐛 GitHub Issues: Report bugs or suggest improvements

💬 Zama Discord: Join community discussions — discord.gg/zama-ai

📄 License

BSD-3-Clause-Clear License
See the LICENSE
 file for full text.