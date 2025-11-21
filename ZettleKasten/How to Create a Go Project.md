**Tags:** #Golang #Programming #ProjectSetup #Development #Tutorial

---

### Definition

A comprehensive guide to **creating a Go project** from scratch, covering module initialization, project structure, dependency management, and development environment setup.

---

### 1. Basic Steps to Create a Go Project

When you start a new Go project, you usually do:

```bash
go mod init <module-name>
```

and then

```bash
go mod tidy
```

Here's what each command actually does:

---

### 2. `go mod init <module-name>`

- **Purpose**: Initializes a new Go module in your current directory.
- **What it does**:
    - Creates a `go.mod` file.
    - The `go.mod` file records:
        - The module name (like a package namespace).
        - The Go version you are targeting.
            
- **Why it matters**:
    - Go modules are the modern way to handle dependencies and versioning.
    - They make your project self-contained.

Example:

```bash
go mod init main
```

This will create `go.mod` containing:

```go
module main  go 1.22
```

---

### 3. `go mod tidy`

- **Purpose**: Cleans up your `go.mod` and `go.sum` files.
- **What it does**:
    - Adds missing dependencies used in your code.
    - Removes dependencies you no longer use.
    - Creates or updates the `go.sum` file, which locks down exact versions for reproducibility.
- **Why it matters**:
    - Keeps your module's dependency graph correct and lean.
    - Ensures your builds are reproducible across different environments.

---

### 4. Other Useful Things You Can Do

**Create a basic project structure**:

```bash
mkdir cmd pkg internal touch cmd/main.go
```

Explanation:

- `cmd/` - Your application entry point(s).
- `pkg/` - Reusable Go packages for external use.
- `internal/` - Reusable Go packages for internal project use only.

**Initialize Git** (recommended):

```bash
git init
```

This helps you track code changes and makes it easier to upload the project to a repository like GitHub.

**Install VSCode Extensions**:

- Install the **Go** extension (official, by Google)
- It provides IntelliSense, linting, debugging, and code navigation.

**Set Up Basic Linting/Formatting**: Inside VSCode settings, enable:

- `gofmt` (built-in formatter)
- `golangci-lint` (for advanced linting)

**Optionally Create a Makefile for Automation**: Example `Makefile`:

```Makefile
run: go run ./cmd/main.go  
build: go build -o bin/app ./cmd/main.go  
tidy: go mod tidy
```

### Personal Insight

Proper project setup is foundational to Go development success. The module system (go mod) has standardized Go project management, making dependency handling far more reliable than the old GOPATH approach. Taking time to set up a good project structure early pays dividends as the project grows.

---

### Related Notes

- [[Go Functions Overview]]
- [[Go Structs Overview]]
- [[Git]]