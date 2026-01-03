# wgpu-ltc-area-lighting

A Rust/WebAssembly demo for Linearly Transformed Cosines using wgpu. This
project builds a WASM package and deploys it to GitHub Pages for easy web-based
visualization.

## Demo
You can view the live demo [here](https://cryze.github.io/wgpu-ltc-area-lighting/).

## Features
- Real-time rendering with wgpu
- Linearly Transformed Cosines technique
- WebAssembly build for browser usage

## Getting Started

### Prerequisites
- Rust (with wasm32-unknown-unknown target)
- wasm-bindgen-cli
- Node.js (optional, for local testing)

### Building Locally
1. Install Rust and add the WASM target:
   ```sh
   rustup target add wasm32-unknown-unknown
   ```
2. Install wasm-bindgen CLI:
   ```sh
   cargo install wasm-bindgen-cli
   ```
3. Build the project:
   ```sh
   cargo build --release --target wasm32-unknown-unknown
   wasm-bindgen --target web --out-dir pkg target/wasm32-unknown-unknown/release/wgpu_linear_cosine_lighting.wasm
   ```
4. Open `index.html` in your browser. Ensure `pkg/` is next to `index.html`.

## Project Structure
```
├── src/                # Rust source files
├── pkg/                # Generated WASM and JS bindings
├── index.html          # Demo web page
├── build-wasm.bat      # Windows build script
├── Cargo.toml          # Rust project manifest
├── .github/workflows/  # GitHub Actions workflow
```
