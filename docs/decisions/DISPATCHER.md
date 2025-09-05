# Command Dispatcher

## ADR-001: Command-line subcommands

### Context

The program, via different subcommands/flags, should perform different actions/task.
some commands might need flags as well.

### Rationale

Similar to git commands.

```shell
./command character create "Conan"
./command character create "Conan" --class="Barbarian" --race="Human"
```

---

## ADR-002: Command-line subcommands + switch statement

### Context

Decided the command style, how do we address different command.

### Rationale

Assuming args[1] is the main command using the switch statement we can direct to the right handler and pass the right 
arguments.

### Consequences

Each handler needs to use the same switch statement mechanism for subcommands, not the greatest.

---

## ADR-003: Command registry pattern

### Context

Investigate how to replace the switch statements.  

### Rationale

Register commands (name, function to execute) in a map of commands.

```go
type CommandRegistry struct {
	commands map[string]*Command
}

var registry = &CommandRegistry{
	commands: make(map[string]*Command),
}
```

### Consequences

Better than the switch statement but doesn't still not great for handling subcommands

---

## ADR-004: init function

### Context

Reading [The Go Programming Language](https://www.gopl.io/) I discovered the init function.


### Rationale

I want to use it to register commands instead of manual wiring.
Handler function become a `Command` struct.
Register function doesn't need a string because uses `Command.Name`.
Handler is outside `init` function so can be tested.

```go
func init() {
    Register(&Command{
        Name:        "character",
        Description: "List all character",
        Usage:       "command character",
        Examples: []string{
        "command character # List of characters",
        },
        Handler: handleCreate,
    })
}

func handleCreate(d *Dispatcher, args []string) error {
    _, _ = fmt.Fprintf(d.Stdout, "  📁 Created character: %s\n", args[2])
    return nil
}
```

### Consequences

Better than the switch statement but doesn't still not great for handling subcommands