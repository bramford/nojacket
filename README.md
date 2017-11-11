NoJacket
==================================================
_Not Just Another Configuration, and Execution Tool_
_NOJACkET_


Overview
-----------------------------

DISCLAIMER: This is currently a learning/experimental project and may never achieve the documented goals

Frustrated by the slow and erroneous nature of using most COE (Configuration, Orchestration and Execution) tools, this project hopes to solve 

Features
-----------------------------

When compared to existing COE tools/systems, _nojacket_ aims to include:

### New features
- Type-safe, inferred, turing complete configuration language (i.e. ocaml itself, potentially with ppx for better UX)
- Supports diff mode - compares the current and last commits/runs/state to only change what needs to change
- Ability to calculate all changes up front (i.e. gather state before any tasks are run)
- No runtime dependencies required (compiles to, then runs as binary machine code)
- Changes require a built-in test to prove success (can be disabled)
- Supports MirageOS unikernels

### Existing features
- Defaults to running tasks in the order they're defined
- No agent required (i.e. *push* mode using SSH)
- Decent templating library (e.g. jinja/jingoo)
- Easy 
- Parallelism
- Nodes can 
- Control node can run as a server, accepting connections from self-bootsrapped nodes (i.e. *pull* mode)

### Limitations
- All execution *modules/libraries* must be (or have bindings) written in OCaml

Milestones
-----------------------------

### Compilation, SSH and execution

- [ ] Compile a basic binary that sets a state
- [ ] Establish an SSH tunnel
- [ ] Execute the binary over the ssh tunnel

#### On-the-fly compilation and execution over persistent SSH tunnel

- [ ] Background SSH tunnel
- [ ] Compile new binary while running
- [ ] Execute new binary over backgrounded SSH tunnel

### Configuration language

#### Task Definition

- [ ] Define a simple task definition data type

##### Conditions
##### Built-in tests

#### Inventory

- [ ] Define a simple inventory host data type

### Command-line interface

- [ ] Basic CLI that runs and executes based on configuration

### State comparison

1. Gather state up-front
2. Calculate differences between desired and current state
3. Compile executable
4. Execute

#### Textual diff comparison mode

- [ ] Conforms to git diff patch style
