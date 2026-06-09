<p align="center">
  <a href="https://unpins.org">
    <img src="unpins-logo.svg" alt="unpins" width="360">
  </a>
</p>

<p align="center">
  Unpin your programs from your OS
</p>

Common programs as single self-contained binaries, built natively for Linux, macOS, and Windows. [unpins](https://unpins.org) curates and builds them; the [`unpin`](https://github.com/unpins/unpin) CLI installs them, or anything from a GitHub release.

The catalog — 70+ programs, from `ffmpeg` and `python` to `vim` and `jq` ([full list](https://unpins.org/packages.html)) — is reproducible from source, and the builds run on old or minimal systems, not just the latest OS.

## The installer

The [`unpin`](https://github.com/unpins/unpin) CLI fetches a program from a GitHub release, verifies its SHA256, then runs it or drops it in `PATH`:

```bash
unpin ffmpeg -version              # run once, nothing installed (the default)
unpin install htop                 # install from the catalog
unpin install BurntSushi/ripgrep   # install from any GitHub release
```

To install `unpin` itself (no root needed):

```bash
curl -fsSLo unpin "https://unpins.org/unpin-$(uname -m)-linux"   # …-darwin on macOS
chmod +x unpin
./unpin install
```

On Windows, fetch [unpin-x86_64-windows.exe](https://unpins.org/unpin-x86_64-windows.exe) and run `.\unpin.exe install`.

## For contributors

Each repo here is a single package recipe (one flake, one binary). Shared build helpers in [`nix-lib`](https://github.com/unpins/nix-lib) and [`action-build`](https://github.com/unpins/action-build); architecture, per-platform gotchas, and patch recipes in [`docs`](https://github.com/unpins/docs).

Issues and PRs welcome on any repo.
