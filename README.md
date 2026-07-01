# homebrew-coda

Homebrew tap for Coda — a native macOS terminal workspace for running Claude
Code across git worktrees.

## Install

```sh
brew tap isaacarnold/coda
brew trust isaacarnold/coda    # one-time — see "Why the trust step?" below
brew install --cask coda
```

Coda is signed and notarized by Apple, so it opens with no Gatekeeper warning,
including on managed/locked-down Macs.

## Why the trust step?

Coda isn't in Homebrew's official catalog — it's distributed through this
personal **tap** (a third-party install repository). Starting with Homebrew 6,
Homebrew refuses to load casks from non-official taps until you explicitly trust
them, as a supply-chain safety measure: it makes you opt in to each outside
source rather than silently running install recipes from anywhere. Apps in the
official `homebrew/cask` catalog (e.g. `brew install --cask <app>`) skip this
because that catalog is trusted by default.

`brew trust isaacarnold/coda` records this tap in your local
`~/.homebrew/trust.json` as one you allow. It's:

- **One-time** — you run it once per machine, ever.
- **No login/token** — the tap and release are public; nothing to authenticate.
- **Persistent** — it survives `brew upgrade`, so updates need no re-trust.

You can undo it anytime with `brew untap isaacarnold/coda`.

## Update

```sh
brew upgrade --cask coda
```

No re-trust needed — trust is per-tap and persists across upgrades.
