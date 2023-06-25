# OpenBook Market Maker
![img2.png](img2.png)

An [HFT](https://cointelegraph.com/news/how-does-high-frequency-trading-work-on-decentralized-exchanges) market making client for the [OpenBook DEX](https://github.com/openbook-dex/program) on Solana.

Create custom trading strategies for SOL and SPL token markets.

---
## Getting Started

 1. Installation Guide: [SETUP.md](SETUP.md)
 2. Client Architecture: [ARCHITECTURE.md](ARCHITECTURE.md)
 3. SOL/USDC Strategy: [OpenBookSolUsdc.java](../src/main/java/com/mmorrell/strategies/openbook/sol/OpenBookSolUsdc.java#L146)

### Adding New Strategy

- Create class MyNewStrategy `extends Strategy`.
- Create bean of MyNewStrategy using `@Component` annotation, or in a config.
- Override `void start()` from the Strategy interface with business logic.
- Wire `MyNewStrategy` bean into `StrategyManager` constructor.
- Add `myNewStrategy.start()` call inside of `StrategyManager.strategyStartup()`.

---
## Contributing

Anyone is welcome to create an issue to build, discuss or request a new feature or update to the existing code base.

The general flow for making a contribution:

- 1. Fork the repo on GitHub
- 2. Clone the project to your own machine
- 3. Commit changes to your own branch
- 4. Push your work back up to your fork
- 5. Submit a Pull request so that we can review your changes

**NOTE**: Be sure to merge the latest from "upstream" before making a
pull request!

---
## Additional Notes

- The current state is a proof-of-concept, but the project is being modularized in this repo.

---
## License

- MIT 