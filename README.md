# Cursor Meta Template Project

This repository is a foundational template demonstrating how to effectively leverage Cursor AI and meta-programming techniques to rapidly bootstrap robust software through clear specifications, compiler-driven feedback, and automated meta-rules.

## Overview
This project serves as a practical example inspired by the blog posts:

- ["You are using Cursor AI incorrectly..."](https://ghuntley.com/you-are-using-cursor-ai-incorrectly)
- ["Yes, Claude Code can decompile itself. Here's the source code"](https://ghuntley.com/claude-code-can-decompile-itself)

The core idea is to showcase a powerful new methodology for using Cursor and similar AI coding assistants by employing:

- **Specification-driven development**: Clearly defined specifications guiding the entire project.
- **Meta-driven development**: Using rules ("stdlib") to automate commits, code hygiene, and ensure consistency.
- Leveraging strongly-typed languages (such as Rust/Haskell) for high-quality automated code generation.

## What is this Project?

This project is a template demonstrating the optimal way to use Cursor and similar AI-driven coding assistants through the concept of **Specification Domains** and multi-agent parallel sessions. It provides foundational setup including:

- Automated specification-driven development
- Automated Git commit workflows
- Compiler-driven development with rapid iteration
- Multi-agent concurrent development ("Multi-Boxing")

## Getting Started

### Prerequisites

Ensure you have installed:

- [Rust and Cargo](https://rustup.rs/)
- [Cursor IDE](https://cursor.so)

## How to Use

### Step 1: Clone the Repository

```bash
git clone <repo-url>
cd groundhog
```

### Step 2: Set Up Cursor Rules

The `.cursor` directory contains rules for automating your coding workflow. Feel free to extend these rules based on your project's specific needs.

### Step 2: Define Specifications

All specifications are organized under `specs/`:

- **Functional Specifications:** located in `specs/`
- **Technical Rules (Meta-rules):** located in `.cursor/`

Update and expand these specifications as needed.

### Step 2: Bootstrapping the Project

Run Cursor with the provided specifications:

- Launch multiple Cursor IDE sessions simultaneously, each handling separate directories (use multi-boxing).
- Cursor agents operate independently in isolated directories, automatically committing incremental changes based on rules defined in `.cursor/`.

### Step 3: Building and Validating the Project

Iterate using this general workflow prompt:

```plaintext
Study @SPECS.md for functional specifications.
Study @.cursor for technical requirements.
Implement what is not implemented.
Create tests.
Run a "cargo build" and verify the application works.
Run "cargo clippy" and resolve linting errors.
```

Repeat this until the implementation meets your expectations.

## Project Structure

```
src/
  ├── core/          # Core functionality
  ├── tracing/logging setup
  └── ...

specs/
├── core
├── ui
└── <other specification domains>

.cursor/
├── auto_commit.md
├── rust_best_practices.md
└── <additional meta-rules>
```

## Key Techniques Demonstrated

- **Multi-Boxing LLMs:** Run multiple Cursor IDE instances concurrently, each with its own specification domain.
- **Specification Domains:** Clearly separate application functionalities to maximize parallel development.
- **Automated Commits:** Every change automatically triggers a Git commit.
- **Bootstrapping:** Automating the generation of rules and the project itself.

## Benefits

- Faster iterative development
- Automatic enforcement of code standards and practices
- Easily extendable specifications
- Empowerment through first-principles understanding of AI-assisted coding tools

## Learn More

- [Original Groundhog Repo](https://github.com/ghuntley/groundhog)
- [Cursor IDE documentation](https://cursor.so/docs)

Enjoy exploring this new coding meta! Contributions and stars are appreciated.
