
🖼️ ERC-721 NFT Marketplace (Frontend)
A decentralized NFT Marketplace frontend built with React and Ethers.js, allowing users to connect their wallet, mint NFTs, list them for sale, and purchase NFTs. This is the frontend-only part; smart contracts are deployed separately.

🚀 Features
Wallet Integration: Connect and disconnect MetaMask easily.

Mint NFTs: Provide a name, description, and image to mint NFTs (metadata stored on IPFS via Pinata).

Marketplace: Browse all NFTs listed for sale.

My NFTs: View your owned NFTs and manage listings.

Buy NFTs: Purchase NFTs securely, with automatic ETH transfer.

Cancel Listings: Delist NFTs anytime before sale.

Error Handling: Clear feedback for all user actions and transactions.

🛠 Tech Stack
Frontend	Libraries & Tools
React.js	UI and component framework
Ethers.js	Blockchain interactions
IPFS/Pinata	NFT metadata storage
Vercel	Hosting and deployment
CSS / HTML	Styling and structure

📦 Installation
1️⃣ Clone the repository

bash
Copy
Edit
git clone https://github.com/Atharva-Joshi8999/NFT_MarketPlace_Frontend.git
cd nft-marketplace
2️⃣ Install dependencies

bash
Copy
Edit
npm install
3️⃣ Set up environment variables

Create a .env file in the root folder:

env
Copy
Edit
REACT_APP_PINATA_API_KEY="YOUR_PINATA_API_KEY"
REACT_APP_PINATA_SECRET_KEY="YOUR_PINATA_SECRET_KEY"
REACT_APP_PINATA_JWT="YOUR_PINATA_JWT_TOKEN"
REACT_APP_CONTRACT_ADDRESS="DEPLOYED_CONTRACT_ADDRESS"
4️⃣ Run frontend locally

bash
Copy
Edit
npm start
Open in your browser: http://localhost:3000
