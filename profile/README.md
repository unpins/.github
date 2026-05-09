# Unpins

[Unpins](https://unpins.org) is an organization dedicated to providing static binaries for Linux, macOS and Windows, built with **Nix** and **Flakes**. Our mission is to "unpin" your essential tools from the constraints of your host distribution's package manager and glibc version.


## 🚀 The Philosophy

Standard package managers often tie you to outdated versions. By leveraging Nix, we build self-contained binaries that run anywhere — from an ancient Debian stable to a minimalist container, a fresh macOS, or a vanilla Windows machine.

- **Portable:** no dependencies, no daemons. Just download and run.
- **Reproducible:** every binary is built via Nix Flakes for 100% auditability.
- **GitHub-native:** binaries live in GitHub releases — the infrastructure you already trust.


## 🛠 The Installer

The [`unpin`](https://github.com/unpins/unpin) CLI is our lightweight package manager. It fetches binaries directly from GitHub releases, verifies the SHA256, and drops each tool in `PATH` ready to run.

```bash
# Install a tool from this org
unpin install htop # or just unpin htop

# Or any project from GitHub releases
unpin install jgm/pandoc

# Run once, without installing
unpin run tree
```


## 📦 Repositories

Each repo hosts a single package recipe (one flake, one tool). The set is intentionally small and curated — focused on widely-used CLI utilities that don't already ship official portable binaries.

Shared building blocks live in [`nix-lib`](https://github.com/unpins/nix-lib); CI glue in [`action-build`](https://github.com/unpins/action-build).


## Status

The `unpin` CLI works today. We're actively adding more packages.

Issues and PRs welcome on any repo.
