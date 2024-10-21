# ds-toolkit 🧰

A data structures library for JavaScript and TypeScript, with performance optimized by Rust and WebAssembly.

This library provides a comprehensive set of data structures with improved performance, leveraging the efficiency of Rust 🚀 and seamlessly integrating into both JavaScript and TypeScript projects. 

It aims to be:

* **Comprehensive:** Covering a wide range of basic and advanced data structures 📚.
* **Type-safe:** Provides type definitions for TypeScript users, ensuring a smooth and type-safe development experience 🔒.
* **Well-documented:** Providing clear explanations and usage examples for both JavaScript and TypeScript developers 📖.
* **Performant:** Implemented in Rust and compiled to WebAssembly for increased efficiency 💪.

## Data Structures Included

1️⃣ **Basic:**
   - Linked List (Singly, Doubly, Circular)
   - Stack
   - Queue (FIFO, Priority Queue)

2️⃣ **Trees:**
   - Binary Search Tree
   - AVL Tree
   - Red-Black Tree
   - B-Tree
   - Trie

3️⃣ **Graphs:**
   - Adjacency list

4️⃣ **Advanced:**
   - Heap (Min-Heap, Max-Heap)
   - Treap
   - LRU Cache
   - LFU Cache

5️⃣ **Probabilistic**
   - Bloom Filter
   - Count-Min Sketch
   - HyperLogLog
   - Skip List

## Documentation 

🚧 TODO

## Installation 

🚧 TODO

## Usage 

🚧 TODO

## Benchmark 

🚧 TODO

## Contribution

### Building ds-toolkit

Building ds-toolkit requires a [supported version of Node and Rust](https://github.com/neon-bindings/neon#platform-support).

To run the build, run:

```sh
$ npm run build
```

This command uses the [@neon-rs/cli](https://www.npmjs.com/package/@neon-rs/cli) utility to assemble the binary Node addon from the output of `cargo`.

### Exploring ds-toolkit

After building ds-toolkit, you can explore its exports at the Node console:

```sh
$ npm i
$ npm run build
$ node
> require('.').greeting()
{ message: 'hello node' }
```

### Available Scripts

In the project directory, you can run:

#### `npm run build`

Builds the Node addon (`index.node`) from source, generating a release build with `cargo --release`.

Additional [`cargo build`](https://doc.rust-lang.org/cargo/commands/cargo-build.html) arguments may be passed to `npm run build` and similar commands. For example, to enable a [cargo feature](https://doc.rust-lang.org/cargo/reference/features.html):

```
npm run build -- --feature=beetle
```

#### `npm run debug`

Similar to `npm run build` but generates a debug build with `cargo`.

#### `npm run cross`

Similar to `npm run build` but uses [cross-rs](https://github.com/cross-rs/cross) to cross-compile for another platform. Use the [`CARGO_BUILD_TARGET`](https://doc.rust-lang.org/cargo/reference/config.html#buildtarget) environment variable to select the build target.

#### `npm run release`

Initiate a full build and publication of a new patch release of this library via GitHub Actions.

#### `npm run dryrun`

Initiate a dry run of a patch release of this library via GitHub Actions. This performs a full build but does not publish the final result.

#### `npm test`

Runs the unit tests by calling `cargo test`. You can learn more about [adding tests to your Rust code](https://doc.rust-lang.org/book/ch11-01-writing-tests.html) from the [Rust book](https://doc.rust-lang.org/book/).

### Project Layout

The directory structure of this project is:

```
ds-toolkit/
├── Cargo.toml
├── README.md
├── lib/
├── src/
|   ├── index.mts
|   └── index.cts
├── crates/
|   └── ds-toolkit/
|       └── src/
|           └── lib.rs
├── platforms/
├── package.json
└── target/
```

| Entry          | Purpose                                                                                                                                  |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------|
| `Cargo.toml`   | The Cargo [manifest file](https://doc.rust-lang.org/cargo/reference/manifest.html), which informs the `cargo` command.                   |
| `README.md`    | This file.                                                                                                                               |
| `lib/`         | The directory containing the generated output from [tsc](https://typescriptlang.org).                                                    |
| `src/`         | The directory containing the TypeScript source files.                                                                                    |
| `index.mts`    | Entry point for when this library is loaded via [ESM `import`](https://nodejs.org/api/esm.html#modules-ecmascript-modules) syntax.       |
| `index.cts`    | Entry point for when this library is loaded via [CJS `require`](https://nodejs.org/api/modules.html#requireid).                          |
| `crates/`      | The directory tree containing the Rust source code for the project.                                                                      |
| `lib.rs`       | Entry point for the Rust source code.                                                                                                          |
| `platforms/`   | The directory containing distributions of the binary addon backend for each platform supported by this library.                          |
| `package.json` | The npm [manifest file](https://docs.npmjs.com/cli/v7/configuring-npm/package-json), which informs the `npm` command.                    |
| `target/`      | Binary artifacts generated by the Rust build.                                                                                            |

Learn more about:

- [Neon](https://neon-bindings.com).
- [Rust](https://www.rust-lang.org).
- [Node](https://nodejs.org).

