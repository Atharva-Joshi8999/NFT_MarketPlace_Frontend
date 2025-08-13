Project: NFT Marketplace
This project is a decentralized application (DApp) for an NFT marketplace. It allows users to connect their MetaMask wallet, mint new NFTs, list their NFTs for sale, and purchase NFTs listed by others. The application interacts with a smart contract on the blockchain to handle all core functionalities.

Key Features
Wallet Integration: Seamlessly connect and disconnect a MetaMask wallet to interact with the DApp.

NFT Minting: Users can mint a new NFT by providing a name, description, and image file. The DApp handles uploading the image and metadata to IPFS and then mints the NFT on the blockchain.

Marketplace: A public marketplace where users can browse all NFTs currently listed for sale.

My NFTs: A dedicated section for users to view all the NFTs they own, whether they are listed for sale or not.

Listing & Delisting: Users can list their owned NFTs on the marketplace for a specific price in ETH. They can also cancel a listing at any time.

Buying: Users can purchase NFTs from the marketplace, with the transaction automatically transferring the NFT to the buyer and the ETH to the seller.

Robust Error Handling: The application includes comprehensive error handling for all major transactions (connecting, minting, buying, listing) to provide clear and informative feedback to the user.

Technologies Used
React: The frontend framework for building the user interface.

Ethers.js: A library for interacting with the Ethereum blockchain, connecting to MetaMask, and managing smart contract calls.

MetaMask: The web3 wallet used by users to sign transactions and manage their crypto assets.

IPFS (Pinata): A decentralized storage network used to store NFT images and metadata, ensuring that the data is permanent and uncensored.

Solidity: The programming language used to write the smart contract that governs the marketplace's logic.

Hardhat/Truffle (Implied): Development environments for compiling and deploying the smart contract.

Getting Started
Prerequisites
Node.js and npm installed.

A code editor like VS Code.

A MetaMask wallet extension installed in your browser.

Access to a blockchain network (e.g., Ethereum testnet like Sepolia).

Installation
Clone the repository:

Bash

git clone [repository-url]
cd [repository-name]
Install dependencies:

Bash

npm install
Set up environment variables:
Create a .env file in the root directory and add your Pinata API keys and JWT token. These are necessary for uploading files and metadata to IPFS.

Code snippet

REACT_APP_PINATA_API_KEY="YOUR_PINATA_API_KEY"
REACT_APP_PINATA_SECRET_KEY="YOUR_PINATA_SECRET_KEY"
REACT_APP_PINATA_JWT="YOUR_PINATA_JWT_TOKEN"
Set up the smart contract:

Deploy your MinterMint.sol smart contract to your chosen network (e.g., Sepolia).

Once deployed, update the CONTRACT_ADDRESS and CONTRACT_ABI in the src/contract.js file with your contract's details.

Run the application:

Bash

npm start
The application will open in your browser at http://localhost:3000.

How to Use
Connect Wallet: Click the "Connect Wallet" button to link your MetaMask account. MetaMask will prompt you to approve the connection.

Mint NFT: Navigate to the "Mint NFT" tab. Fill in the name and description, upload an image, and click "Mint NFT." Approve the transaction in MetaMask, and your NFT will be minted and added to your collection.

View My NFTs: Go to the "My NFTs" tab to see all the NFTs you own. You can list unlisted NFTs for sale or cancel existing listings from here.

Explore Marketplace: Switch to the "Marketplace" tab to see all NFTs currently for sale. You can click "Buy" on any listing to purchase it. Approve the transaction in MetaMask to complete the purchase.

Disconnect: Click the "Disconnect" button to unlink your wallet from the application. Note that for a full disconnect, you may need to manually disconnect from the MetaMask extension as well.

Code Structure Highlights
useEffect Hooks: Used for side effects like checking for existing MetaMask connections on load and listening for account changes.

State Management: useState hooks are used to manage the application's state, including the user's account, contract instances, and various UI elements.

Asynchronous Functions: All blockchain interactions and API calls are handled with async/await to manage asynchronous operations cleanly.

Component-based UI: The entire application is built as a single App component, with conditional rendering used to display different sections (Mint, Marketplace, My NFTs).

Error Handling: The try...catch blocks are used extensively to gracefully handle errors from both the blockchain and API calls, providing user-friendly alerts.







