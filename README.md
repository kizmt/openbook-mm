# OpenBook Market Maker
An HFT market making client for the [OpenBook DEX](https://github.com/openbook-dex/program) on Solana.

This initial guide will focus on configuring the client to market make the [SOL/USDC](https://solscan.io/account/8BnEgHoWFysVcuFFX7QztDmzuH8r5ZFvyP3sYwn1XTh6) pair.

After completeing the guide feel free to explore, customize, and improve upon the client however you see fit.

## Initial Requirements
Please ensure you have installed Java, Docker Desktop, Solana CLI, and your preferred IDE.

- [Java](https://www.java.com/download)
- [Docker Desktop](https://www.docker.com/products/docker-desktop/)
- [IntelliJ](https://www.jetbrains.com/idea/download)
- [Solana CLI](https://docs.solana.com/cli/install-solana-cli-tools)
- Paid RPC Service - [QuickNode](https://www.quicknode.com/)


We recommend that all users [generate a new solana keypair](https://solanacookbook.com/references/keypairs-and-wallets.html#how-to-generate-a-new-keypair) for this initial exercise.

## Configuration
To configure the client for market making SOL/USDC, you will require the following keys:

- Your Wallet Pubkey
- Your [Wallet Private Key](https://solanacookbook.com/references/keypairs-and-wallets.html#how-to-generate-a-new-keypair) in a JSON file
- The USDC Token Account for that wallet
- The SOL/USDC Open Orders Account for that wallet

Please follow the initial configuration steps for market making SOL/USDC

### OpenBookConfig.java

### OpenBookSolUsdc.java

### OpenBookTest.java

### Resources
- Configure openbook.properties with your RPC URL link
- Add your Solana Private key .json file to the resources folder

## Deployment
Use Docker for easy deployment
1. Build the Container from the repository Dockerfile
2. Configure the container name, instance name, and port bindings
3. Run the image
4. Profit


- Installation Guide: [SETUP.md](SETUP.md)
