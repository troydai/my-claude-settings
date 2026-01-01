# My Claude Settings

Shared Claude Code configuration repository. Clone as a git submodule in other repositories to share settings and hooks across projects.

## Usage

### 1. Add as a submodule

```bash
git submodule add <repository-url> .claude-settings
```

### 2. Create symlink

```bash
ln -s .claude-settings/settings .claude
```

### 3. Initialize submodule (for cloning existing repos)

```bash
git submodule update --init --recursive
```

## Contents

### Settings (`settings/settings.json`)

- **Hooks**: Session start hook for remote environment setup
- **Permissions**: Pre-approved commands for `git`, `gh`, `cat`, `gwt`, and `gwtree`

### Hooks (`settings/hooks/`)

#### `session-start.sh`

Runs on session start in Claude Code remote environments (`CLAUDE_CODE_REMOTE=true`). Performs:

- Installs `rustup` if not present
- Installs Rust toolchain from `rust-toolchain.toml` if present
- Installs GitHub CLI (`gh`) via apt-get or GitHub releases

## License

See [LICENSE](LICENSE) for details.
