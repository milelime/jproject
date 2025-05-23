# Java Project Helper Script (`jproject`)

A simple Bash script to streamline the creation, compilation, and execution of
basic Java projects compatible with Eclipse.

## Features

- Create an Eclipse-compatible Java project structure
- Generate Java classes or interfaces with proper directory layout and packages
- Compile all Java source files
- Run a specified main class
- Optional Git repository initialization
- Installable man page for command-line documentation

## Installation

### 1. Install the script

Place the script in your `PATH` and make it executable:

```bash
sudo cp jproject /usr/local/bin/
sudo chmod +x /usr/local/bin/jproject
```

### 2. Install the man page

Save the accompanying jproject.1 man page in your project folder.

#### Copy it to the appropriate man section directory

```bash
sudo mkdir -p /usr/local/share/man/man1
sudo cp jproject.1 /usr/local/share/man/man1/
```

#### Update the man database

```bash
sudo mandb
```

### 3. Verify installation

```bash
which jproject
man jproject
```

## Usage

```bash
jproject <command> [args]
```

## Commands

| Command     | Description                                  |
| ----------- | -------------------------------------------- |
| `project`   | Create a new Eclipse-compatible Java project |
| `class`     | Create a new Java class                      |
| `interface` | Create a new Java interface                  |
| `compile`   | Compile all `.java` files into `bin/`        |
| `run`       | Compile and run a specified main class       |
| `test`      | Run tests (currently a placeholder)          |

## Examples

```bash
jproject project
jproject class
jproject interface
jproject compile
jproject run
```

## Running the Project

When using jproject run, you’ll be prompted to enter the fully qualified main
class name, e.g., com.example.Main.

## Requirements

- Bash
- Java Development Kit (JDK): javac and java in your PATH
- Git (optional, for project initialization)

## License

MIT License.
