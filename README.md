# killFlow

**Predictive input buffer for Geometry Dash 2.2081**  
Developer: Lumin  
Mod ID: `lumin.killflow`  
Geode SDK: `5.11.2`

killFlow is an MIT-licensed fork/adaptation of the Afterflow 2.2.7 source
provided for this project. The original MIT copyright and permission notice
is retained in `LICENSE`. The predictive simulation and input interception
architecture are derived from that source; the branding, metadata, UI palette,
and logo have been adapted for killFlow.

## Included functionality

- Live gameplay input interception through the Geometry Dash
  `GJBaseGameLayer::handleButton` hook.
- A detached ghost-player simulation that evaluates candidate input delays.
- Queued press/release handling and delivery of buffered inputs.
- Per-mode buffer stages and configurable stage keybinds.
- In-game control panel and draggable mobile K launcher.
- Recent prediction log, stage controls, and configurable UI styling.
- Red glow / red-to-black K branding.

## Targets

- Windows
- Android 32-bit
- Android 64-bit

The source retains platform-conditional code from the upstream project;
the packaged mod metadata currently advertises Windows and Android only.

## Build requirements

- Geode SDK `5.11.2`
- Geometry Dash `2.2081` bindings
- CMake `3.29+`
- Geode CLI
- Android NDK for Android builds

```bash
export GEODE_SDK=/path/to/geode-sdk
geode build -p windows
geode build -p android
```

The Geode CLI/toolchain determines Android ABI packaging. For CI, use the
included GitHub Actions workflow.

## Important

This is source code, not a compiled `.geode` release. Build it against the
matching SDK and bindings, then test on each target. Predictive buffering can
change gameplay timing; use practice mode while validating it.
