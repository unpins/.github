<p align="center">
  <a href="https://unpins.org">
    <img src="unpins-logo.svg" alt="unpins" width="360">
  </a>
</p>

<p align="center">
  Unpin your programs from your OS
</p>

Common programs as single self-contained binaries, built natively for Linux, macOS, and Windows. [unpins](https://unpins.org) curates and builds them; the [`unpin`](https://github.com/unpins/unpin) CLI installs them, or anything from a GitHub release.

The catalog builds are reproducible from source and run on old or minimal systems, not just the latest OS.

## The installer

The [`unpin`](https://github.com/unpins/unpin) CLI fetches a program from a GitHub release, verifies its SHA256, then runs it or drops it in `PATH`:

```bash
unpin ffmpeg -version              # run once, nothing installed (the default)
unpin install htop                 # install from the catalog
unpin install BurntSushi/ripgrep   # install from any GitHub release
```

To install `unpin` itself, download a build from [unpins.org](https://unpins.org).

## For contributors

Each repo here is a single package recipe (one flake, one binary). Shared build helpers in [`nix-lib`](https://github.com/unpins/nix-lib) and [`action-build`](https://github.com/unpins/action-build); architecture, per-platform gotchas, and patch recipes in [`docs`](https://github.com/unpins/docs).

Issues and PRs welcome on any repo.
