Below is an updated README for the organization, highlighting the two key projects:

---

# Qubic-Qulang

Qubic-Qulang is an organization dedicated to building a decentralized marketplace for AI inference powered by Qubic technology. Our ecosystem combines smart contracts, blockchain-based payments, and modern web interfaces to empower anyone to become an AI provider and for users to access AI inference services using Qubic tokens.

## Key Projects

### 1. qulang-app (Main dApp)
- **URL:** [http://46.17.103.110:3000/](http://46.17.103.110:3000/)
- **Description:**  
  The qulang-app is our primary decentralized application, providing a modern, responsive interface for interacting with the Qubic smart contracts. Users can easily connect their wallets, view balances, top up accounts, and initiate AI inference requests.  
- **Features:**  
  - Multi-wallet connection (e.g., MetaMask, private seed, vault file)
  - Real-time transaction monitoring and balance updates
  - Seamless interaction with on-chain smart contracts for account management and payments

### 2. example-openai-provider
- **API URL:** [http://46.17.103.110:3001/](http://46.17.103.110:3001/)
- **Chatbot Playground:** [http://46.17.103.110:3001/debug](http://46.17.103.110:3001/debug)
- **Description:**  
  This Next.js application serves as a demonstration of how an AI provider can register on our marketplace. The API exposes model information such as provider name, image, and description from environment variables. It also features a playground with a chatbot for testing and debugging AI inference.
- **Features:**  
  - Simple API for retrieving provider details
  - Chatbot playground to interact with the AI model
  - Automated deployment setup with Docker and GitHub Actions

## Organization Overview

Our ecosystem consists of:

- **On-chain Smart Contracts (HM25):**  
  Developed in C++ using Qubic’s framework, these smart contracts manage user balances, provider registrations, and AI inference transactions. They include functions like Topup, Withdraw, and ProcessRequest with a built-in fee and burn mechanism.

- **Decentralized Infrastructure:**  
  Qubic’s node software, compiled in EFI, enforces blockchain transactions and wallet management. The system is designed for scalability (supporting up to 2^20 users) and real-time processing.

- **Centralized Services via dApp:**  
  Our main dApp (qulang-app) acts as the primary interface for users and providers. It handles connection management, real-time transaction tracking, and serves as the hub for AI inference interactions, while a PostgreSQL database stores supplementary information such as detailed model data and endpoints.

## How to Contribute

We welcome contributions from the community. To contribute:

1. Fork a repository and create a feature branch.
2. Make your changes and submit a pull request.
3. Follow our coding guidelines and include tests where applicable.

For detailed contribution guidelines, please refer to the [Contributing Documentation](./doc/contributing.md).

## Contact

For questions, feedback, or collaboration proposals, please reach out via our GitHub issue tracker or join our community on Discord.

## License

All projects in the Qubic-Qulang organization are released under the [Anti-Military License](./LICENSE.md).

---

This README emphasizes our main dApp (qulang-app) along with the example-openai-provider, providing clear access URLs and descriptions of their functionalities.
