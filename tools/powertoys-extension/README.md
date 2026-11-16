# Wasla PowerToys Command Palette / PowerToys Run Extension (`wasla-ptrun`)

`wasla-ptrun` is a standalone, zero-dependency Rust helper that connects Windows launcher tools (PowerToys Command Palette, PowerToys Run, Flow Launcher, Raycast for Windows) to Wasla's [Local Authenticated API](../../docs/api.md).

## Building

```powershell
cargo build --release --manifest-path tools/powertoys-extension/Cargo.toml
```

## Prerequisites

1. Open **Wasla → Settings → Local automation API** and turn on **Enable local automation API**.
2. Wasla writes `%LOCALAPPDATA%\Wasla\api-token.json` containing the loopback port (`53320`) and a 256-bit Bearer token.

## Usage

### Querying Palette Items

```powershell
wasla-ptrun query ""
wasla-ptrun query "ring"
wasla-ptrun query "https://wasla.dev"
```

Outputs a JSON array of palette commands (`send-clipboard`, `ring`, `camera` `photo`/`scan`, `send-url`, `send-text`, plus recent timeline items).

### Invoking an Action

```powershell
wasla-ptrun invoke ring
wasla-ptrun invoke send-clipboard
wasla-ptrun invoke camera photo
wasla-ptrun invoke camera scan
wasla-ptrun invoke send-url "https://wasla.dev"
wasla-ptrun invoke send-text "Copied from PowerToys"
wasla-ptrun invoke send-file "C:\Users\Alice\Desktop\notes.pdf"
```
