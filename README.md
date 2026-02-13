# password-manager
> A lightweight terminal-based password manager developed in Java.

This project provides a quick and efficient way to store and manage non-important passwords directly from your terminal, utilizing Base64 for basic data obfuscation.

---

## Features
* **Ease of Use:** Designed for quick storage and retrieval of daily-use credentials.
* **Obfuscation:** Utilizes B64 encoding to ensure passwords are not stored in plain text.
* **Clean Architecture:** Uses a `src` and `bin` structure to keep source code and bytecode separate.

---

## Setup & Installation

Before running the application, you must compile the source code. Ensure you have the JDK (Java Development Kit) installed.

### 1. Build the Project
Run these commands from the project root:
```bash
# Create the bin directory for compiled files
mkdir bin

# Compile all source files into the bin folder
javac -d bin src/*.java
```
### 2. How to Run (Bytecode & Executable .jar)

## Option A. Bytecode
Run this immediately after compiling to start the application.
```bash
# Windows, macOS, and Linux
java -cp bin Main
```

## Option B. Executable .jar

### 1. Create the .jar
```bash
jar cvfe PasswordManager.jar Main -C bin .
```

### 2. Run the .jar
```bash
java -jar PasswordManager.jar
```

---

## Security Disclaimer

Note: This application uses *Base64 encoding* for password storage.
* **Encoding vs. Encryption:** Base64 is an encoding scheme used to hide plain-text visibility; it is **not** a secure cryptographic encryption method (like AES).

* **Intended Use:** This tool is intended only for **"non-important"** passwords where quick access is prioritized over high-level security. Do not use this for banking or sensitive primary accounts.

---

## Project Structure

- password-manager-java/: # parent folder
- src/:          Human-readable .java source files
- bin/:          Compiled .class bytecode (generated at build)
- README.md:     Project documentation

---

## License

This project is open-source and available under the MIT License.

---

# TODO:
* refactor project
* add encryption rather than B64 encoding
