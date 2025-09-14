# WasmCraft
Project for HackCMU 2025

## Local Build
```sh
$ cargo build
```

## Web Build

```sh
$ trunk serve
```

### Notes on WASM

Need to remove our dependency on the async feature of wasmtime, this should all let us get out patch size for our fork of wasmtime smaller and actually allow code execution to work on the web.

Alternatives:
- Queue events from wasm, and only apply them on each timer tick
- Sync blocking (idk prob bad to block bevy's thread pool)

Other problems
- need to reset the code timer on reset event
