# homebrew-coda

Homebrew tap for [Coda](https://github.com/IsaacArnold/coda) — a native macOS
terminal workspace for running Claude Code across git worktrees.

## Install

```sh
brew tap isaacarnold/coda
brew trust isaacarnold/coda    # one-time: Homebrew 6+ requires trusting non-official taps
brew install --cask coda
```

Coda is signed and notarized by Apple, so it opens with no Gatekeeper warning,
including on managed/locked-down Macs.

## Update

```sh
brew upgrade --cask coda
```

No re-trust needed — trust is per-tap and persists across upgrades.
