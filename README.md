# btcx_api



## Deployment

- Docker support via `Dockerfile`
- Deploy to [Fly.io](https://fly.io/) using `fly.toml` configuration
- The server binds to `0.0.0.0:8080` by default

### 11. API Server (api/src/main.rs)

- HTTP server using Actix-web
- Endpoint: POST /create_tx to create unsigned Bitcoin transactions
- Accepts inputs (txid, vout) and outputs (address, amount)
- Returns hex-encoded transaction
- Binds to 0.0.0.0:8080

### Supporting Files

- Build script (`scripts/build/build.sh`): Builds all tools in release or debug mode
- Dockerfile: Containerizes the API server
- fly.toml: Fly.io deployment configuration
- Cargo.toml files: Dependency specifications for each crate

### Development

- **Dependency Management:** Automated via Dependabot for Cargo packages
- **Dependencies:** All Rust crates defined in respective `Cargo.toml` files
- **Language:** Rust (systems programming language, memory safe)

## Probability Note

This project is primarily for educational purposes. The odds of finding an address with some bitcoins in it per cycle are approximately 2.94×10⁻³¹ to 1, assuming there are about 100 million seeds in use. This probability is extremely low, reflecting the vastness of the seed space and the security of Bitcoin's design. Alternatively, as a ratio, the odds are 1 to 3.4×10³⁰.

## License

[Add your license information here]

## Contributing

[Add contribution guidelines here]