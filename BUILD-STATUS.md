# killFlow v0.2.0 build status

## Implemented in source
- Real `GJBaseGameLayer::handleButton` interception for player input.
- Press/release prediction through the `intercept(...)` path.
- Candidate-delay simulation using detached ghost players.
- Buffered press/release queue and delivery logic.
- Game-mode-aware stage configuration.
- In-game panel, stage controls, live log, and mobile draggable launcher.
- K-only logo asset and red/black UI defaults.

## Not verified in this environment
- A Geode `.geode` package has **not** been compiled here.
- This environment does not have `GEODE_SDK` configured and has no `geode` CLI.
- Windows, Android32, and Android64 runtime behavior still needs device testing.

## Build in GitHub Actions
1. Create a GitHub repository and upload this project.
2. Ensure the default branch is `main`.
3. Open **Actions** and run **killFlow Build** (or push a commit).
4. Download each `killFlow-*` artifact and install the matching `.geode`.

Use Geometry Dash 2.2081 and Geode SDK 5.11.2 for this source revision.
