# 🕸️ Wasm Runtime Comparison

> **Comparison matrix of all WebAssembly runtimes. Don't just list them, compare them.**

Build Status: [![Matrix Check](https://img.shields.io/badge/Matrix-Updated-green)](https://github.com/wasmruntime-io/wasm-runtime-comparison) 
License: [![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

## ⚡ The Matrix

Which WebAssembly runtime should you use? This table compares the most popular runtimes based on language, execution model, standards support, and primary use cases.

| Runtime | Written In | Execution Mode | WASI Support | Component Model | Key Focus / "Killer Feature" | License |
| :--- | :---: | :---: | :---: | :---: | :--- | :---: |
| **[Wasmtime](https://wasmtime.dev/)** | Rust | JIT / AOT | ✅ (Preview 2) | ✅ | **The Standard.** Built by Bytecode Alliance. Secure, fast, reference implementation. | Apache-2.0 |
| **[WasmEdge](https://wasmedge.org/)** | C++ | AOT / JIT / Interpreter | ✅ | ✅ | **Cloud Native & AI.** Optimized for Kubernetes and AI inference extensions. | Apache-2.0 |
| **[Wasmer](https://wasmer.io/)** | Rust | JIT / AOT / Static | ✅ | ✅ | **The Ecosystem.** Has its own package manager (WAPM) and "run anywhere" philosophy. | MIT |
| **[WAMR](https://github.com/bytecodealliance/wasm-micro-runtime)** | C | Interpreter / AOT / JIT | ✅ | 🚧 | **IoT & Embedded.** Small footprint (Intel), meant for resource-constrained devices. | Apache-2.0 |
| **[Wazero](https://wazero.io/)** | Go | JIT / Interpreter | ✅ | 🚧 | **Zero Dependencies.** Pure Go runtime, no CGO required. Perfect for Go integration. | Apache-2.0 |
| **[Wasm3](https://github.com/wasm3/wasm3)** | C | Interpreter | ⚠️ (Basic) | ❌ | **Portability.** The fastest WebAssembly *interpreter*. Runs on almost any CPU/MCU. | MIT |
| **[V8](https://v8.dev/)** | C++ | JIT (TurboFan) | ❌ (Node/Browser APIs) | ❌ | **Browser/JS.** The engine powering Chrome and Node.js. | BSD |
| **[SpiderMonkey](https://spidermonkey.dev/)** | C++ | JIT | ❌ | 🚧 | **Browser (Firefox).** First to support many Wasm proposals. | MPL-2.0 |
| **[Second State (SSVM)](https://github.com/second-state/SSVM)** | C++ | AOT | ✅ | ❌ | *Now merged into WasmEdge.* | - |

> **Legend:**
> * ✅ = Full / Stable Support
> * 🚧 = In Progress / Experimental
> * ⚠️ = Partial / Limited Support
> * ❌ = Not Supported / Not Applicable
> * **JIT**: Just-In-Time Compilation | **AOT**: Ahead-Of-Time Compilation

## 🔍 Detailed Comparisons

### Performance Tier
* **Tier 1 (Near Native):** Wasmtime, Wasmer, WasmEdge (AOT mode)
* **Tier 2 (Balanced):** V8, SpiderMonkey
* **Tier 3 (Start-up focused / Low resource):** Wasm3, WAMR (Interpreter mode)

### Use Case Recommendations
* **Running inside a Go binary?** 👉 Choose **Wazero**.
* **Need standard compliance & security?** 👉 Choose **Wasmtime**.
* **Doing AI inference or running on K8s?** 👉 Choose **WasmEdge**.
* **Running on a microcontroller (ESP32, etc.)?** 👉 Choose **WAMR** or **Wasm3**.

## 🤝 Contribution

Found a mistake or want to add a new runtime?
1. Fork this repository.
2. Edit `README.md`.
3. Update the Matrix row.
4. Submit a Pull Request.

---
*Maintainer note: This matrix is manually curated. Please provide sources for feature support claims.*
