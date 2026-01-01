# Changelog

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.1.0/).

## [0.1.0] - 2026-01-01

### Added

- Initial project structure with `settings/` directory
- `settings.json` with Claude Code configuration
  - SessionStart hook configuration
  - Permission rules for common CLI tools (`git`, `gh`, `cat`, `gwt`, `gwtree`)
- `hooks/session-start.sh` for remote environment setup
  - Automatic `rustup` installation
  - Rust toolchain installation from `rust-toolchain.toml`
  - GitHub CLI (`gh`) installation via apt-get or GitHub releases
  - Resilient error handling for partial success scenarios
