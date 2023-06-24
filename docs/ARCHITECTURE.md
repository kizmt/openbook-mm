## Architecture

- `OpenBookSolUsdc` extends `Strategy`
    - implements `start()`
- `Strategy` contains 1 void method `start()`

Future:
- `OpenBookSolUsdc` extends `OpenBookStrategy`
    - Provides `marketId`
    - implements `start()`
- `OpenBookStrategy` extends `Strategy`


TBD