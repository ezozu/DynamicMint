# DynamicMint - On-Demand NFT Generation & Deployment

DynamicMint provides a framework for dynamically generating and deploying Non-Fungible Tokens (NFTs) based on user-defined parameters. This repository contains the core Typescript libraries and tools required to build customizable NFT minting platforms, allowing for the creation of unique digital assets in real-time. This solution is designed for developers who need a robust and scalable system for personalized NFT creation, simplifying the complex process of smart contract interaction and asset generation.

DynamicMint addresses the need for flexible NFT minting solutions that go beyond static image uploads. It enables the creation of NFTs with dynamic metadata, configurable properties, and on-chain randomization. This makes it ideal for projects involving generative art, personalized collectibles, and game assets. The framework prioritizes modularity and extensibility, allowing developers to easily integrate custom logic and data sources into the minting process. By abstracting away the complexities of blockchain interaction, DynamicMint empowers developers to focus on the creative aspects of NFT design and distribution.

This repository offers a complete solution encompassing smart contract deployment, metadata generation, and front-end integration examples. It leverages industry-standard libraries like Ethers.js for secure and efficient blockchain communication. The core logic is implemented in Typescript, ensuring type safety and maintainability. The included example projects demonstrate how to build a user interface for customizing NFT properties and triggering the minting process. Through its modular architecture and comprehensive documentation, DynamicMint provides a solid foundation for building innovative NFT experiences.

## Key Features

*   **Dynamic Metadata Generation:** Generates NFT metadata on-demand based on user-provided parameters. This allows for unique traits and properties to be assigned to each NFT at the time of minting. Technically, this is achieved by passing user inputs through a configuration file which maps these inputs to specific metadata fields.

*   **Smart Contract Deployment and Interaction:** Deploys a customizable ERC-721 smart contract and provides helper functions for interacting with it. The deployment process is automated using Hardhat, and the interaction is facilitated by Ethers.js. The contract address and ABI are stored in a configuration file for easy access.

*   **Customizable NFT Properties:** Defines a schema for NFT properties, allowing developers to specify the types and ranges of values that can be set by users. This schema is enforced both on the front-end and in the smart contract, ensuring data integrity. The schema is represented as a JSON object which can be easily modified to add new traits or modify existing ones.

*   **On-Chain Randomization:** Integrates a mechanism for generating random numbers on-chain to influence NFT properties. This can be used to create NFTs with unpredictable traits, adding an element of surprise for users. Randomness is generated using Chainlink VRF or other on-chain randomness solutions, depending on the chosen network.

*   **Front-End Integration Examples:** Includes example React components for building a user interface for customizing NFT properties and triggering the minting process. These components provide a starting point for building a custom minting platform. The examples showcase the use of Ethers.js for connecting to the blockchain and interacting with the smart contract.

*   **Modular Architecture:** Designed with a modular architecture, allowing developers to easily integrate custom logic and data sources into the minting process. This includes the ability to customize the metadata generation process, the smart contract logic, and the front-end interface. This is achieved through a series of well-defined interfaces and abstract classes.

## Technology Stack

*   **Typescript:** Used for the core logic and smart contract development, ensuring type safety and maintainability. Typescript provides static typing, which helps prevent errors and makes the code easier to understand and refactor.

*   **Ethers.js:** A popular Javascript library for interacting with the Ethereum blockchain. It is used for connecting to the blockchain, interacting with the smart contract, and signing transactions.

*   **Hardhat:** A development environment for Ethereum software. It is used for compiling, testing, and deploying the smart contract.

*   **Solidity:** The programming language used for writing smart contracts on the Ethereum blockchain.

*   **React (Example):** A popular Javascript library for building user interfaces. The example projects use React to demonstrate how to build a front-end for customizing NFT properties and triggering the minting process.

## Installation

1.  Clone the repository:
    git clone https://github.com/ezozu/DynamicMint.git

2.  Navigate to the project directory:
    cd DynamicMint

3.  Install dependencies:
    npm install

4.  Install Hardhat dependencies within the smart_contracts directory:
    cd smart_contracts
    npm install @openzeppelin/contracts hardhat

5. Return to the root directory:
    cd ..

## Configuration

1.  Create a `.env` file in the root directory.

2.  Add the following environment variables:


3.  Modify the `hardhat.config.ts` file in the `smart_contracts` directory to include your Infura API key and private key. Ensure the network configuration matches your chosen Ethereum network.

4. Modify the configuration file (e.g., `config.json` or similar) to specify the NFT properties schema, metadata templates, and other project-specific settings. This file dictates how dynamic parameters map to the generated NFT.

## Usage

1.  Compile the smart contract:
    cd smart_contracts
    npx hardhat compile

2.  Deploy the smart contract:
    npx hardhat deploy --network <your_network>

3.  Set the `CONTRACT_ADDRESS` environment variable to the address of the deployed contract.

4.  Run the example front-end (if applicable):
    cd example_frontend
    npm start

5.  Use the API provided by the DynamicMint library to generate NFT metadata and mint NFTs. The API provides functions for connecting to the blockchain, interacting with the smart contract, and signing transactions. Specific details on API endpoints are in the `docs/api.md` file.

    Example (using Ethers.js):


## Contributing

We welcome contributions to DynamicMint! Please follow these guidelines:

1.  Fork the repository.

2.  Create a new branch for your feature or bug fix.

3.  Write tests for your code.

4.  Submit a pull request with a clear description of your changes.

5.  Follow code style and conventions used in project.

## License

This project is licensed under the MIT License. See the [LICENSE](https://github.com/ezozu/DynamicMint/blob/main/LICENSE) file for details.

## Acknowledgements

This project utilizes libraries and concepts from the open-source Ethereum development community. We are grateful for the contributions of the Ethers.js, Hardhat, and OpenZeppelin teams.