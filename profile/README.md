# Qubic-Qulang

Qubic-Qulang is an organization dedicated to building a decentralized marketplace for AI inference powered by Qubic technology. Our ecosystem combines smart contracts, blockchain-based payments, and modern web interfaces to empower anyone to become an AI provider and for users to access AI inference services using Qubic tokens.

## Key Projects

### 1. qulang-app (Main dApp)
- **URL:** [http://46.17.103.110:3000/](http://46.17.103.110:3000/)
- **Repository:** [https://github.com/Qubic-Qulang/qulang-app](https://github.com/Qubic-Qulang/qulang-app)
- **Description:**  
  The qulang-app is our primary decentralized application, providing a modern, responsive interface for interacting with the Qubic smart contracts. Users can easily connect their wallets, view balances, top up accounts, and initiate AI inference requests.  
- **Features:**  
  - Multi-wallet connection (e.g., MetaMask, private seed, vault file)
  - Real-time transaction monitoring and balance updates
  - Seamless interaction with on-chain smart contracts for account management and payments

### 2. example-openai-provider
- **API URL:** [http://46.17.103.110:3001/](http://46.17.103.110:3001/)
- **Chatbot Playground:** [http://46.17.103.110:3001/debug](http://46.17.103.110:3001/debug)
- **Repository:** [https://github.com/Qubic-Qulang/example-openai-provider](https://github.com/Qubic-Qulang/example-openai-provider)
- **Description:**  
  This Next.js application serves as a demonstration of how an AI provider can register on our marketplace. The API exposes model information such as provider name, image, and description from environment variables. It also features a playground with a chatbot for testing and debugging AI inference.
- **Features:**  
  - Simple API for retrieving provider details
  - Chatbot playground to interact with the AI model
  - Automated deployment setup with Docker and GitHub Actions

### 3. core
- **Repository:** [https://github.com/Qubic-Qulang/core](https://github.com/Qubic-Qulang/core)
- **Description:**  
  The Qubic Core is the node software running the Qubic network. It is written in C++ (a QuLang fork) and handles blockchain interactions and smart contract execution.
