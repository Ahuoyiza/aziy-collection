## Aziy - The Learning Revolution NFT Collection (Candy Machine)

This README file provides instructions on deploying and interacting with the Aziy NFT collection created using the Solana Candy Machine and Phantom wallet.

**Prerequisites:**

* Node.js and npm (or yarn) installed on your system.
* A Solana developer account with sufficient SOL for deployment fees.
* A Phantom wallet installed and configured with your Solana account.

**Deployment:**

1. **Clone this repository:**

   ```bash
   git clone https://github.com/your-username/aziy-nft-collection.git
   ```

2. **Install dependencies:**

   ```bash
   cd aziy-nft-collection
   npm install
   ```

3. **Update configuration:**

   - Open the `candy-machine-config.js` file.
   - Update the following fields:
        - ` Solana_program_library_address`: Replace with the address of the @solana/spl-token library (obtain from the Solana devnet documentation).
        - `treasury_account`: Replace with the public key of your Solana wallet where you want to receive SOL from NFT sales.
        - `gatekeeper`: Set to `null` for a public mint (no gatekeeping). 
        - You can explore other configuration options in the file for customizing the mint price, supply, etc.

4. **Build the Candy Machine:**

   ```bash
   npm run build
   ```

5. **Deploy the Candy Machine:**

   ```bash
   npm run deploy
   ```

   - This command will prompt you for your Solana wallet's private key. Enter it securely (it won't be stored anywhere).
   - The script will deploy the Candy Machine to the Solana devnet and print the Candy Machine ID.

**Minting with Phantom Wallet:**

1. **Open the Candy Machine minting website** (replace `<candy_machine_id>` with the ID obtained from deployment):

   ```
   https://beta.nft-launchpad.com/solana/candy-machine/<candy_machine_id>
   ```

2. **Connect your Phantom wallet** to the website.

3. **Follow the on-screen instructions** to initiate the minting process. You may need to approve the transaction with your Phantom wallet.

4. **Once successful, your Aziy NFT will be deposited** into your Phantom wallet. 

**Additional Notes:**

* This is a basic setup for demonstration purposes. Consider security best practices when deploying Candy Machines on a mainnet.
* You can explore further customization options provided by the Candy Machine documentation.
* For testing purposes, you can use faucets to obtain SOL for your developer account on the Solana devnet.

**Resources:**

* Solana Candy Machine: [https://www.quicknode.com/guides/solana-development/nfts/how-to-create-a-solana-nft-collection-using-candy-machine-v3-and-typescript](https://www.quicknode.com/guides/solana-development/nfts/how-to-create-a-solana-nft-collection-using-candy-machine-v3-and-typescript)
* Phantom Wallet: [https://phantom.app/](https://phantom.app/)
* Solana Devnet: [https://explorer.solana.com/?cluster=devnet](https://explorer.solana.com/?cluster=devnet)


