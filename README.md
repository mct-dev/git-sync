# git-sync

A bash script that updates the main branch of all git repositories in a directory, in parallel.

## Installation

```bash
# Clone the repo
git clone https://github.com/mct-dev/git-sync.git

# Make it available in your PATH
ln -s $(pwd)/git-sync/git-sync /usr/local/bin/git-sync
```

## Usage

```bash
# Update all repos in current directory
git-sync

# Update all repos in a specific directory
git-sync ~/projects
```

## Features

- Automatically detects the default branch (main or master)
- Updates repos in parallel (default: 10 concurrent operations)
- Skips repos with uncommitted changes
- If you're on a different branch, updates the main branch without switching
- Colored output for easy status tracking

## Configuration

| Environment Variable | Description | Default |
|---------------------|-------------|---------|
| `GIT_SYNC_PARALLEL` | Maximum parallel operations | 10 |

## License

MIT
