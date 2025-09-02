# Go Life Sim

![GitHub go.mod Go version](https://img.shields.io/github/go-mod/go-version/matteo-gildone/go-life-sim)
![GitHub License](https://img.shields.io/github/license/matteo-gildone/go-life-sim)

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
- [ ] All commands output correct messages but no real implementation

##  Commands

### Basic commands

| Command name | Description       | Implementation |
|--------------|-------------------|----------------|
| `init`       | Initialise app    | ❌              |
| `help`       | List all commands | ❌              |

### Character commands

| Command name              | Description          | Implementation |
|---------------------------|----------------------|----------------|
| `list`                    | List of characters   | ❌              |
| `create <character name>` | Create new character | ❌              |
| `help`                    | List all subcommands | ❌              |

### Class commands

| Command name   | Description               | Implementation |
|----------------|---------------------------|----------------|
| `list`         | List of classes           | ❌              |
| `<class name>` | Assign class to character | ❌              |
| `help`         | List all subcommands      | ❌              |

### Job commands

| Command name   | Description             | Implementation |
|----------------|-------------------------|----------------|
| `list`         | List of jobs            | ❌              |
| `<class name>` | Assign job to character | ❌              |
| `help`         | List all subcommands    | ❌              |

## 📚Resources

- [The Go Programming Language](https://www.gopl.io/)
- [Command Line Interface Guidelines](https://clig.dev/)

---

**Note**: This is a learning project. The implementation prioritizes clean code, proper testing and Go best practise over
feature completeness
