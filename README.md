# prebuild-pcsclite-win

Build `@pokusew/pcsclite` native addon for Windows x64 + Node.js 22.

## Usage

1. Push this repo to GitHub
2. GitHub Actions will automatically compile on Windows
3. Download the artifact `pcsclite-win-x64-node22`
4. Place `pcsclite.node` into the warehouse-desktop build:
   ```
   warehouse-desktop/prebuilds/win32-x64/pcsclite.node
   ```
5. Rebuild the desktop app

## Why?

`@pokusew/pcsclite` uses `node-gyp` + `nan` and links against the Windows
Smart Card API (`winscard.dll`). It cannot be cross-compiled from macOS.
