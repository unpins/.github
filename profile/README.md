<p align="center">
  <a href="https://unpins.org">
    <img src="unpins-logo.svg" alt="unpins" width="360">
  </a>
</p>

Static, single-binary builds of common CLI tools for Linux, macOS, and Windows — built reproducibly with **Nix Flakes**, distributed through GitHub releases. No glibc pinning, no system dependencies, no daemons. Just download and run.

→ Browse and install at **<https://unpins.org>**.

## The installer

The [`unpin`](https://github.com/unpins/unpin) CLI fetches binaries from GitHub releases, verifies the SHA256, and drops each tool in `PATH` ready to run:

```bash
unpin install htop          # curated package from this org
unpin install jgm/pandoc    # or any GitHub release
unpin run tree              # run once, no install
```

Install `unpin` itself: see <https://unpins.org>.

## For contributors

Each repo here is a single package recipe (one flake, one tool). Shared build helpers in [`nix-lib`](https://github.com/unpins/nix-lib) and [`action-build`](https://github.com/unpins/action-build); architecture, per-platform gotchas, and patch recipes in [`docs`](https://github.com/unpins/docs).

Issues and PRs welcome on any repo.
