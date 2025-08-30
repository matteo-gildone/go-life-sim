# Go Life Sim

A git-inspired command-line interface for creating life sim app and explore Italian folklore.
Built with Go and designed for speed, simplicity and extensibility.

## 🏗️ Installation

### From source
```bash
git clone git@github.com:matteo-gildone/go-life-sim.git
cd go-life-sim
make build
./bin/gls init
```

## 🧪 Development

### Prerequisites
- Go 1.21 or higher
- Make (optional, for build scripts)

## 🙏 Acknowledgment

- Inspired by Git's elegant command-line interface
- Built with Go's powerful standard library (no third party packages)

## 🚀 Phases

### Phase 1

- [ ] Project structure
- [ ] Make file
- [ ] Dispatcher package
- [ ] Auto register commands in the init function
- [ ] All commands print something but nothing is created (no real implementation)

##  Commands

### Basic commands

| Command name | Description       | Implementation |
|--------------|-------------------|----------------|
| `init`       | Initialise app    | ❌              |
| `help`       | List all commands | ❌              |

### Character commands

| Command name | Description          | Implementation |
|--------------|----------------------|----------------|
| `create`     | Create new character | ❌              |
| `help`       | List all subcommands | ❌              |

### Class commands

| Command name         | Description               | Implementation |
|----------------------|---------------------------|----------------|
| `class`              | List of classes           | ❌              |
| `class <class name>` | Assign class to character | ❌              |
| `help`               | List all subcommands      | ❌              |

## 📚Resources

- [The Go Programming Language](https://www.gopl.io/)
- [Command Line Interface Guidelines](https://clig.dev/)

---

**Note**: This is a learning project. The implementation prioritizes clean code, proper testing and Go best practise over
feature completeness
