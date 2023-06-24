# OpenBook Market Maker
![img2.png](img2.png)

An [HFT](https://cointelegraph.com/news/how-does-high-frequency-trading-work-on-decentralized-exchanges) market making client for the [OpenBook DEX](https://github.com/openbook-dex/program) on Solana.
### Installation Guide: [SETUP.md](SETUP.md)
### SOL/USDC Strategy: [OpenBookSolUsdc.java](../src/main/java/com/mmorrell/strategies/openbook/sol/OpenBookSolUsdc.java#L146)

---
## Adding New Strategy

- Create class MyNewStrategy `extends Strategy`.
- Create bean of MyNewStrategy using `@Component` annotation, or in a config.
- Override `void start()` from the Strategy interface with business logic.
- Wire `MyNewStrategy` bean into `StrategyManager` constructor.
- Add `myNewStrategy.start()` call inside of `StrategyManager.strategyStartup()`.

## Architecture

- `OpenBookSolUsdc` extends `Strategy`
  - implements `start()`
- `Strategy` contains 1 void method `start()`

Future:
- `OpenBookSolUsdc` extends `OpenBookStrategy`
  - Provides `marketId`
  - implements `start()`
- `OpenBookStrategy` extends `Strategy`

## Additional Notes

- The current state is a proof-of-concept, but the project is being modularized in this repo.

## License

- MIT 