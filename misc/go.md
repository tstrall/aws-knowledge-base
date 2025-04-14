# Go (Golang)

**What it is:**
- A statically typed, compiled language designed by Google
- Known for simplicity, concurrency primitives, and fast execution
- Popular in DevOps tooling, networking, and backend services

---

## Core Features

| Feature        | Description |
|----------------|-------------|
| **Goroutines** | Lightweight threads managed by the Go runtime |
| **Channels**   | Typed conduits for goroutine communication |
| **Interfaces** | Implicit contracts for polymorphism |
| **Packages**   | Every Go project is made up of packages (no classes) |
| **Error handling** | Explicit errors via return values, no exceptions |

---

## Hello World
```go
package main
import "fmt"

func main() {
    fmt.Println("Hello, world!")
}
```

---

## Goroutines and Channels
```go
func printMsg(msg string) {
    fmt.Println(msg)
}

func main() {
    go printMsg("async") // runs concurrently
    printMsg("sync")
}
```

```go
ch := make(chan string)
go func() { ch <- "ping" }()
msg := <-ch
fmt.Println(msg)
```

---

## Tooling
- `go build` – compile
- `go run` – compile & run
- `go fmt` – auto-format
- `go test` – unit testing
- `go mod` – dependency management

---

## Use Cases
- Kubernetes components and CLIs (e.g., `kubectl`)
- Terraform and Vault (HashiCorp tools)
- Microservices and REST APIs
- High-performance network daemons

---

## Interview Tips
- Know how goroutines work (not 1:1 with OS threads)
- Be able to explain interfaces and type embedding
- Show how Go avoids complex abstractions on purpose
- Use clear examples of performance and concurrency use cases
