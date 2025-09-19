# Structs

## ADR-00N: Template

**Date:** 2024-12-19

### Context

### Decision

### Rationale

### Alternative considered

### Consequences

---

## ADR-001: Config, Character

### Context

I need a way to group fields together to store information used around the CLI.
Each needs to load/write files other than the field needed by each struct.

### Decision

At the moment I only have to "manage" config and character information.

```go
type Config struct {
    configDir string       `json:"config_dir"`
	file string            `json:"file"`
    ActiveCharacter string `json:"active_character"`
}

type Character struct {
    configDir string `json:"config_dir"`
    file      string `json:"file"`
	Name      string `json:"name"`
    Class     string `json:"class"`
    Race      string `json:"race"`
    Xp        int    `json:"xp"`
    Level     int    `json:"level"`
    Hardcore  bool   `json:"hardcore"`
}
```
