# crabfish 🦀♟️

Crabfish is a **chess engine** written from scratch, in rust. 
It can provide a **strong next move** for the current player, or an **evaluation of a board position**.

I've been working on this engine for fun. It's playing strength, based on my tests, 
is around 2000 elo (in the chess.com pool). 
Based on what I've seen, it's tactical play is quite good but it's positional play sucks.

## Install
```bash
cargo install crabfish
```

## Build From Source

```bash
git clone https://github.com/MonliH/crabfish.git
cd crabfish
cargo run --release
```

Note: the `--release` flag when building is **VERY IMPORTANT**.
The engine can not search very deep without the optimizations provided by it.

## Usage
You can either use the cli program, with the `move` subcommand, help:
```bash
./target/release/crabfish move --help
```

Or, if you want to use a chess gui supporting the UCI proticol, launch the engine with the `uci` argument in your gui:
```bash
./target/release/crabfish uci
```

## Techniques

* Negamax
* Alpha-Beta pruning
* Iterative deepening
* Principal Variation Search
* Null-move heuristic
* Reverse futility pruning
