# OpenBook Market Maker
An [HFT](https://cointelegraph.com/news/how-does-high-frequency-trading-work-on-decentralized-exchanges) market making client for the [OpenBook DEX](https://github.com/openbook-dex/program) on Solana.

This guide will focus on initial configuration and setting up the client to trade the [SOL/USDC](https://solscan.io/account/8BnEgHoWFysVcuFFX7QztDmzuH8r5ZFvyP3sYwn1XTh6) pair.

## Initial Requirements
Please ensure you have installed Java, Docker Desktop, Solana CLI, and your preferred IDE.

- [Java](https://www.java.com/download)
- [Docker Desktop](https://www.docker.com/products/docker-desktop/)
- [Solana CLI](https://docs.solana.com/cli/install-solana-cli-tools)
- [IntelliJ](https://www.jetbrains.com/idea/download)
- RPC Service - [QuickNode](https://www.quicknode.com/)

You will require a paid RPC service to operate the client, you may wish to ignore this until you have completed all other steps.

## Solana Account Requirements
We recommend that all users [generate a new solana keypair](https://solanacookbook.com/references/keypairs-and-wallets.html#how-to-generate-a-new-keypair) for this exercise.

To configure the client for market making SOL/USDC, you will require the following account keys:

- Your Solana Wallet [Pubkey](https://solanacookbook.com/references/keypairs-and-wallets.html#how-to-generate-a-new-keypair)
    - This is your public Solana wallet address [(see example)](https://solscan.io/account/dooMxPqm1c2tfHmU74afb29RmFq537Jrdmro8eKXHNf)
- Your wallet [Private Key](https://solanacookbook.com/references/keypairs-and-wallets.html#how-to-generate-a-new-keypair) in a JSON file
    - Default file location: ```~/.config/solana/id.json```
- The USDC Token Account _for that wallet_ 
    - ```USDC_QUOTE_WALLET ("your-usdc-token-account")``` [(see example)](https://solscan.io/account/2LHzRXq2uXXbyTFhgPSSRQxbj3FZChGNzsSr1eFH7Ljf)
- The SOL/USDC Open Orders Account _for that wallet_
    - ```SOL_USDC_OOA ("your-sol-usdc-open-orders-account")``` [(see example)](https://solscan.io/account/F8ijbW2wxjPY7Aa7QknLybwKHYk5QVkN1q5BU8aGNqhS)

## Configuration

Fork the repostiory and run your own local build through your preferred IDE.
From here we will look to insert the required Solana account keys into the following files;
- OpenBookConfig.java
- OpenBookSolUsdc.java
- OpenBookTest.java

### Resources
- Configure openbook.properties with your RPC URL link
- Add your Solana Private key .json file to the resources folder

## Testing

When ready, run OpenBookTest.java to confirm set up has successlly completed

## Deployment
Use Docker for easy deployment
1. Build the Container from the repository Dockerfile
2. Configure the container name, instance name, and port bindings
3. Run the image
4. Profit


- Installation Guide: [SETUP.md](SETUP.md)
