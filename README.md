# OpenBook Market Maker
An HFT market making client for the [OpenBook DEX](https://github.com/openbook-dex/program) on Solana.

This initial guide will focus on configuring the client to market make the [SOL/USDC](https://solscan.io/account/8BnEgHoWFysVcuFFX7QztDmzuH8r5ZFvyP3sYwn1XTh6) pair.

After completeing the guide feel free to explore, customize, and improve upon the client however you see fit.

## Initial Requirements
Please ensure you have installed Java, Docker Desktop, Solana CLI, and your preferred IDE.

- [Java](https://www.java.com/download)
- [Docker Desktop](https://www.docker.com/products/docker-desktop/)
- [Solana CLI](https://docs.solana.com/cli/install-solana-cli-tools)
- [IntelliJ](https://www.jetbrains.com/idea/download)
- RPC Service - [QuickNode](https://www.quicknode.com/)

You will require a paid RPC service to operate the client, you may wish to ignore this step until you have completed inital setup.

We recommend that all users [generate a new solana keypair](https://solanacookbook.com/references/keypairs-and-wallets.html#how-to-generate-a-new-keypair) for this initial exercise.

## Configuration
To configure the client for market making SOL/USDC, you will require the following keys:

- Your Wallet Pubkey (see above)
- Your [Wallet Private Key](https://solanacookbook.com/references/keypairs-and-wallets.html#how-to-generate-a-new-keypair) in a JSON file ```~/.config/solana/id.json```
- The USDC Token Account for that wallet ```USDC_QUOTE_WALLET ("your-usdc-token-account")```
- The SOL/USDC Open Orders Account for that wallet ```SOL_USDC_OOA ("your-sol-usdc-open-orders-account")```

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
