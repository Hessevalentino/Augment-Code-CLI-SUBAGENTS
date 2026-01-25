# 🤖 Augment Code CLI Subagents

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Open Source](https://badges.frapsoft.com/os/v1/open-source.svg?v=103)](https://opensource.org/)
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg)](http://makeapullrequest.com)
[![GitHub Stars](https://img.shields.io/github/stars/Hessevalentino/Augment-Code-CLI-SUBAGENTS?style=social)](https://github.com/Hessevalentino/Augment-Code-CLI-SUBAGENTS)

A curated collection of specialized AI agents for Augment Code CLI, designed to provide expert assistance across different development domains. Each agent is a domain expert with deep knowledge in specific areas of software development.

## 📋 Overview

This repository contains configuration files for specialized AI subagents that can be used with [Augment Code CLI](https://www.augmentcode.com/). Each agent is meticulously crafted to be an expert in a specific domain, providing focused, professional, and highly effective assistance for various development tasks.

**Why use specialized agents?**
- **Domain Expertise**: Each agent has deep knowledge in its specific area
- **Consistent Quality**: Agents follow established best practices and methodologies
- **Time Saving**: Get expert-level assistance without context switching
- **Educational**: Learn from detailed explanations and professional code examples

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

### 🔵 [Humanizer](agents/humanizer/)
**Professional content writer and AI text humanizer**
- Identifies and removes 24 common AI writing patterns
- Creates natural, engaging content with authentic voice
- Adds personality and human perspective to sterile text
- Preserves original language and meaning

## 🚀 Getting Started

### Prerequisites
- [Augment Code CLI](https://www.augmentcode.com/) installed and configured
- Basic understanding of your development domain

### Installation

Clone this repository to access all agent configurations:

```bash
git clone https://github.com/Hessevalentino/Augment-Code-CLI-SUBAGENTS.git
cd Augment-Code-CLI-SUBAGENTS
```

### Quick Start

1. Browse available agents in the `agents/` directory
2. Read the agent's README to understand its capabilities
3. Load the `agent.md` configuration file in Augment Code CLI
4. Start interacting with your specialized expert assistant

## 📖 Usage

### Directory Structure

Each agent is organized in its own directory under `agents/`:

```
agents/
  └── agent-name/
      ├── agent.md       # Agent configuration (load this in Augment Code CLI)
      └── README.md      # Detailed documentation and capabilities
```

### Using an Agent

**Step 1: Choose Your Agent**
Browse the [Available Agents](#-available-agents) section and select the agent that matches your task.

**Step 2: Review Capabilities**
Read the agent's README to understand what it can do:
```bash
cd agents/openscadag
cat README.md
```

**Step 3: Load in Augment Code CLI**
Load the `agent.md` configuration file in Augment Code CLI according to the [official documentation](https://www.augmentcode.com/).

**Step 4: Start Working**
Interact with your specialized expert assistant. The agent will provide domain-specific guidance, code examples, and best practices.

### Example Workflow

```bash
# Clone the repository
git clone https://github.com/Hessevalentino/Augment-Code-CLI-SUBAGENTS.git

# Explore available agents
cd Augment-Code-CLI-SUBAGENTS/agents
ls -la

# Review a specific agent
cd code-reviewer
cat README.md

# Load agent.md in Augment Code CLI and start coding!
```

## 🛠️ Creating New Agents

Want to contribute a new specialized agent? Great! Follow these guidelines:

### Agent Creation Process

1. **Research**: Study best practices for AI agent design and your domain
2. **Structure**: Create a new directory under `agents/your-agent-name/`
3. **Configure**: Create `agent.md` with YAML frontmatter and instructions
4. **Document**: Write a minimal README.md (max 500 words, no icons)
5. **Update**: Add your agent to the main README with proper links
6. **Test**: Thoroughly test your agent configuration

### Requirements

- Follow the structure defined in `.augmentrules`
- Use lowercase names with hyphens for directories
- Maintain consistency with existing agents
- Define clear expertise boundaries
- Provide concrete examples and methodologies
- Include YAML frontmatter: `name`, `description`, `model`, `color`

See `.augmentrules` for detailed guidelines.

## 📝 Documentation Guidelines

This project follows minimal documentation principles:
- Maximum 500 words per agent README
- No unnecessary supporting documentation
- Professional tone without decorative elements
- Focus on essential information only

## 🤝 Contributing

Contributions are welcome and appreciated! We're looking for:

- **New Agents**: Specialized agents for different development domains
- **Improvements**: Enhancements to existing agent configurations
- **Bug Fixes**: Corrections to agent behavior or documentation
- **Documentation**: Better examples and usage guides

### How to Contribute

1. Fork this repository
2. Create a feature branch (`git checkout -b feature/amazing-agent`)
3. Follow the guidelines in `.augmentrules`
4. Commit your changes (`git commit -m 'Add amazing agent'`)
5. Push to the branch (`git push origin feature/amazing-agent`)
6. Open a Pull Request

### Contribution Guidelines

- Follow the existing agent structure and format
- Adhere to documentation guidelines in `.augmentrules`
- Ensure all file and folder names are lowercase
- Test your agent configurations thoroughly
- Provide clear commit messages
- Update the main README when adding new agents

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 👤 Author

**Valentino Hesse**
- GitHub: [@Hessevalentino](https://github.com/Hessevalentino)

## 🌟 Acknowledgments

- Built for use with [Augment Code](https://www.augmentcode.com/)
- Inspired by the need for specialized AI assistance in software development
- Thanks to all contributors who help improve these agents

## 📊 Project Stats

- **6 Specialized Agents** covering different development domains
- **Open Source** under MIT License
- **Community Driven** - contributions welcome
- **Production Ready** - tested and actively used

## 🔗 Related Resources

- [Augment Code Official Website](https://www.augmentcode.com/)
- [Augment Code Documentation](https://www.augmentcode.com/)
- [Report Issues](https://github.com/Hessevalentino/Augment-Code-CLI-SUBAGENTS/issues)
- [Request Features](https://github.com/Hessevalentino/Augment-Code-CLI-SUBAGENTS/issues/new)

---

**Note:** This is an open source project. Feel free to use, modify, and distribute according to the MIT License terms.

⭐ If you find this project useful, please consider giving it a star on GitHub!

