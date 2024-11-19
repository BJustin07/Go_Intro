# Installing GoLang

GoLang is a modern programming language known for its simplicity, efficiency, and robust performance. Follow the instructions below to install Go on your system.

---

## Prerequisites

- A computer running **Windows**, **macOS**, or **Linux**.
- Administrator rights to install software.
- Access to the internet.

---

## Installing GoLang

### Windows

1. **Download the Go Installer**:
    - Visit the official Go website: [https://golang.org/dl/](https://golang.org/dl/).
    - Download the latest `.msi` installer for Windows.

2. **Run the Installer**:
    - Double-click the downloaded `.msi` file.
    - Follow the installation prompts to complete the setup.

3. **Verify Installation**:
    - Open a **Command Prompt** or **PowerShell**.
    - Run the command:
      ```sh
      go version
      ```
    - You should see the installed Go version.

4. **Setup Environment Variables** (optional if default paths are used):
    - Ensure `C:\Go\bin` is added to your `PATH` system environment variable.

---

### macOS

1. **Download the Go Installer**:
    - Visit the official Go website: [https://golang.org/dl/](https://golang.org/dl/).
    - Download the `.pkg` installer for macOS.

2. **Run the Installer**:
    - Double-click the downloaded `.pkg` file.
    - Follow the on-screen instructions to install Go.

3. **Verify Installation**:
    - Open the **Terminal**.
    - Run the command:
      ```sh
      go version
      ```
    - You should see the installed Go version.

4. **Setup Environment Variables** (optional):
    - Add the Go binary path to your shell profile (e.g., `.zshrc` or `.bash_profile`):
      ```sh
      export PATH=$PATH:/usr/local/go/bin
      ```
    - Reload the profile:
      ```sh
      source ~/.zshrc
      ```

---

### Linux

1. **Download the Go Tarball**:
    - Visit [https://golang.org/dl/](https://golang.org/dl/).
    - Download the appropriate tarball (`.tar.gz`) for your Linux distribution.

2. **Extract and Install**:
    - Open a terminal.
    - Navigate to the directory containing the downloaded file.
    - Run the following commands:
      ```sh
      sudo tar -C /usr/local -xzf go<version>.linux-amd64.tar.gz
      ```
      Replace `<version>` with the downloaded version number (e.g., `1.21.0`).

3. **Setup Environment Variables**:
    - Add the Go binary path to your shell profile (e.g., `.bashrc` or `.zshrc`):
      ```sh
      export PATH=$PATH:/usr/local/go/bin
      ```
    - Reload the profile:
      ```sh
      source ~/.bashrc
      ```

4. **Verify Installation**:
    - Run:
      ```sh
      go version
      ```
    - You should see the installed Go version.

---

## Post-Installation Test

1. **Check Go Workspace**:
    - Create a directory for your Go workspace, e.g., `~/go`.
    - Set the environment variable:
      ```sh
      export GOPATH=~/go
      export PATH=$PATH:$GOPATH/bin
      ```

2. **Write and Run a Test Program**:
    - Create a file `hello.go` with the following content:
      ```go
      package main
 
      import "fmt"
 
      func main() {
          fmt.Println("Hello, Go!")
      }
      ```
    - Run the program:
      ```sh
      go run hello.go
      ```

---

## Troubleshooting

- If `go version` does not return the installed version, ensure the Go binary directory is added to your `PATH`.
- For additional help, consult the official Go documentation: [https://golang.org/doc/](https://golang.org/doc/).

---

## Uninstallation

### Windows
- Use the **Add or Remove Programs** feature to uninstall Go.

### macOS
- Remove the `/usr/local/go` directory:
  ```sh
  sudo rm -rf /usr/local/go
