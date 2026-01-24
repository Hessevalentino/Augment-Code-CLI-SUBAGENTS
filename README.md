# 🤖 Augment Code CLI Subagents

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Open Source](https://badges.frapsoft.com/os/v1/open-source.svg?v=103)](https://opensource.org/)
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg)](http://makeapullrequest.com)

A collection of specialized AI agents for Augment Code CLI, designed to provide expert assistance across different development domains.

## 📋 Overview

This repository contains configuration files for specialized AI subagents that can be used with Augment Code CLI. Each agent is an expert in a specific domain, providing focused and professional assistance for various development tasks.

## 🎯 Available Agents

Each agent is organized in its own directory with a configuration file (`agent.md`) and detailed README.

### 🔵 [OpenSCAD Agent](agents/openscadag/) (openscadag)
**Expert in parametric 3D modeling and optimization**
- OpenSCAD functional programming and CSG operations
- CGAL rendering optimization (15-60× performance improvements)
- 3D printing validation and geometry checking
- Parametric design with Customizer interface

### 🟢 [PSR Fixer](agents/psr-fixer/)
**Automatic PHP Standards Recommendations compliance fixer**
- Adds strict types declarations
- Fixes naming conventions and visibility modifiers
- Ensures PSR-1/PSR-12 compliance
- Automated code formatting

### 🟡 [PSR Auditor](agents/psr-auditor/)
**PHP Standards Recommendations compliance auditor**
- Comprehensive PSR compliance checking
- Detailed violation explanations
- Priority-based issue reporting
- Educational feedback for developers

### 🟣 [Code Reviewer](agents/code-reviewer/)
**Comprehensive code review specialist**
- Logic and correctness analysis
- Design patterns and SOLID principles
- Best practices enforcement
- Constructive and educational feedback

### 🔴 [Penetration Tester](agents/penetration-tester/)
**Security testing and vulnerability assessment**
- Simulates common attack vectors (SQL injection, XSS, CSRF)
- Identifies security vulnerabilities
- Provides exploit scenarios
- Offers remediation guidance

## 🚀 Getting Started

### Prerequisites
- [Augment Code CLI](https://www.augmentcode.com/) installed and configured

### Installation

1. Clone this repository:
```bash
git clone https://github.com/Hessevalentino/Augment-Code-CLI-SUBAGENTS.git
cd Augment-Code-CLI-SUBAGENTS
```

2. Use the agent configuration files with Augment Code CLI according to the official documentation.

## 📖 Usage

Each agent is organized in its own directory under `agents/` with:
- `agent.md` - Agent configuration file with instructions and expertise
- `README.md` - Detailed documentation about the agent's capabilities

To use an agent:

1. Browse the `agents/` directory and select the appropriate agent for your task
2. Load the agent configuration file (`agent.md`) in Augment Code CLI
3. Interact with the specialized agent for your specific needs

Example:
```bash
# Navigate to an agent directory
cd agents/openscadag

# Review the agent's capabilities
cat README.md

# Use agent.md with Augment Code CLI
```

## 🛠️ Creating New Agents

When creating new agents, follow the guidelines in `.augmentrules`:

- Research best practices for AI agent design
- Maintain consistency with existing agents
- Use standardized YAML frontmatter
- Define clear expertise boundaries
- Provide concrete examples and methodologies

## 📝 Documentation Guidelines

This project follows minimal documentation principles:
- Maximum 500 words per agent README
- No unnecessary supporting documentation
- Professional tone without decorative elements
- Focus on essential information only

## 🤝 Contributing

Contributions are welcome! Please feel free to submit a Pull Request. When contributing:

- Follow the existing agent structure and format
- Adhere to the documentation guidelines in `.augmentrules`
- Ensure all file and folder names are lowercase
- Test your agent configurations thoroughly

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 👤 Author

**Valentino Hesse**

## 🌟 Acknowledgments

- Built for use with [Augment Code](https://www.augmentcode.com/)
- Inspired by the need for specialized AI assistance in software development

---

**Note:** This is an open source project. Feel free to use, modify, and distribute according to the MIT License terms.

