<!--
START OF: cli-helper.md
Purpose: Provides usage guidelines for our internal CLI utility used to simplify common workflows.
Update Frequency: Update whenever a new CLI command is added or modified.
Location: docs/internal-tools/cli-helper.md
-->

# Internal CLI Helper

## Overview

This tool simplifies repetitive commands like setup, cleanup, testing, and deployment.

---

## Installation

```bash
chmod +x ./cli.sh
./cli.sh help
```
---

## Available Commands

| Command  | Description                       |
|----------|-----------------------------------|
| `init`   | Initializes the local environment |
| `test`   | Runs all tests                    |
| `deploy` | Deploys current build             |
| `clean`  | Cleans build artifacts            |

---

## Example

```bash
./cli.sh test
```
---

## Structure

- Written in Bash / Node / Python (based on your stack)
- Modular: Add subcommands under /cli-commands/

---

## Add a New Command

1. Create a new script under /cli-commands/

2. Register it in cli.sh

3. Document it above!

<!-- END OF: cli-helper.md -->
