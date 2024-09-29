NFT Bridge from Sepolia to Amoy Using FX Portal! 

In this project, we will batch mint NFTs on the Sepolia network and bridge them to the Amoy network using the FX Portal. This project demonstrates the bridging functionality with ERC721A NFTs.

## Description 

This project shows how to bridge NFTs between different networks. With the deprecation of the Goerli and Mumbai testnets, we are using Sepolia and Amoy networks. The `StreetNft.sol` contract is ideal for batch minting multiple NFTs in one go.

### Smart Contract Example

The `StreetNft.sol` contract includes the following function for batch minting NFTs:



#### Batch Minting NFTs 
Users can batch mint NFTs on the Sepolia network using the batchMintNFT() function. This function allows the minting of multiple NFTs in one transaction.

#### Bridging NFTs 
Once the NFTs are minted on Sepolia, they need to be bridged to Amoy using FX Portal. This involves approving the deposit and waiting for the bridge process to complete.

#### Checking NFT Balances
Verify the successful bridging by checking the balance of NFTs on the Amoy network after the bridge operation.

npm install
Set Up Environment Variables: Create a .env file and configure it with your RPC URLs and wallet private key.

#### Execution Steps
Compile the Contract:

npx hardhat compile
Deploy the Contract on Sepolia Network:

npx hardhat run scripts/deploy.js --network sepolia
Batch Mint NFTs on Sepolia Network:



npx hardhat run scripts/batchMint.js --network sepolia
Approve NFT Deposit for Bridging:



npx hardhat run scripts/approveDeposit.js --network sepolia
Wait for the Bridging Process: Wait for 20-30 minutes for the NFTs to be bridged to the Amoy network. Once completed, copy the contract address on the Amoy network.

#### Check NFT Balance on Amoy Network: 
Deploy and run getBalance.js on the Amoy network to check the total number of NFTs received:


npx hardhat run scripts/getBalance.js --network amoy


 ### Authors
Lokesh Gupta
