# Custom deploy changes (this fork)

1. **Home:** the “Join the ArtCraft community” card is removed.
2. **Web open/upload:** every opened document queues Recognize Text on pages without text
   (`skip_text_pages`). Models download first on wasm if needed.

## Build the web zip

```sh
cargo xtask models
bash packaging/web/package.sh
```

See `packaging/web/README.md`. Serve `.wasm` as `application/wasm` and `.onnx` as
`application/octet-stream` on IIS.
