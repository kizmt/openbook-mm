![img3.png](img3.png)
## Initial Requirements

Please ensure you have installed Java, Docker Desktop, Solana CLI, and your preferred IDE.
- [Docker Desktop](https://www.docker.com/products/docker-desktop/) (for Windows)
- [Solana CLI](https://docs.solana.com/cli/install-solana-cli-tools)
- [IntelliJ](https://www.jetbrains.com/idea/download) (Recommended)
- [RPC Service](https://omniatech.io/pages/solana-rpc/) Provider - [Helius](https://www.helius.dev/pricing/)

You will require a paid RPC service to operate the client, you may wish to ignore this until you have completed all other steps.

---
## Solana Account Requirements

We recommend that all users [generate a new solana keypair](https://solanacookbook.com/references/keypairs-and-wallets.html#how-to-generate-a-new-keypair) for this initial exercise.
To configure the client for market making SOL/USDC, you will require the following account keys:

- Your Solana Wallet [Pubkey](https://solanacookbook.com/references/keypairs-and-wallets.html#how-to-generate-a-new-keypair)
    - This is your public Solana wallet address [(see example)](https://solscan.io/account/dooMxPqm1c2tfHmU74afb29RmFq537Jrdmro8eKXHNf)
    - Usage in Repository: ```("your-solana-pubkey")```
- Your wallet [Private Key](https://solanacookbook.com/references/keypairs-and-wallets.html#how-to-generate-a-new-keypair) in a JSON file
    - Default local file location: ```~/.config/solana/id.json```
    - Rename id.json to your solana pubkey with .json, Usage in Repository: ```("your-solana-pubkey.json")```
- The USDC Token Account _for that Pubkey_
    - Usage in Repository ```("your-usdc-quote-wallet")``` [(see example)](https://solscan.io/account/2LHzRXq2uXXbyTFhgPSSRQxbj3FZChGNzsSr1eFH7Ljf)
- The SOL/USDC Open Orders Account _for that Pubkey_
    - Usage in Repository ```("your-solusdc-ooa")``` [(see example)](https://solscan.io/account/F8ijbW2wxjPY7Aa7QknLybwKHYk5QVkN1q5BU8aGNqhS)

---
## Configuration

Fork the repostiory and open your own local project through your preferred IDE.
From here we will look to insert the above Solana account keys into the following files;
- ```OpenBookTest.java```
- ```OpenBookConfig.java```
- ```OpenBookSolUsdc.java```
- ```openbook.properties```

---
## Resources

- Configure openbook.properties with your RPC URL link
- Add your Solana Private key .json file to the resources **folder**, rename the id.json file to display your wallet Pubkey followed by .json.

---
## Testing

When ready, run ```OpenBookTest.java``` to confirm that all checks have successfully passed. 

---
## Deployment

Use Docker for easy deployment
1. Build the Container from the repository Dockerfile
2. Configure the container name, instance name, and port bindings
   ![img.png](img.png)
3. Run the image
4. Confirm success by checking your open orders over at the [OpenBook Explorer](https://openserum.io)
5. Begin configuring your own SolUsdc trading strategies and profit

---
## Setup Complete

### Links:
- Client Architecture: [ARCHITECTURE.md](ARCHITECTURE.md)
- Customizing your SolUsdc Strategy [OpenBookSolUsdc.java]((../src/main/java/com/mmorrell/strategies/openbook/sol/OpenBookSolUsdc.java#L146))
- Return to Readme [README.md](README.md)