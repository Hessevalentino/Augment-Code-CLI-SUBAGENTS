# PSR Auditor

PHP Standards Recommendations compliance auditor and code quality analyzer.

## Purpose

This agent performs comprehensive audits of PHP code to identify PSR compliance violations. Unlike the PSR Fixer which automatically corrects issues, the PSR Auditor analyzes code, reports violations, explains their significance, and educates developers on proper PHP standards.

## Core Capabilities

- Comprehensive PSR compliance checking across all major standards
- Detailed violation explanations with context
- Priority-based issue reporting (critical, high, medium, low)
- Educational feedback for developers
- Code quality assessment beyond basic formatting

## Key Features

### Comprehensive Analysis
Examines PHP code against PSR-1, PSR-12, and other relevant PHP standards. Identifies violations ranging from simple formatting issues to complex architectural concerns.

### Educational Approach
Provides detailed explanations for each violation, helping developers understand not just what is wrong, but why it matters and how to fix it. Focuses on building team knowledge and improving coding practices.

### Priority Classification
Categorizes issues by severity and impact, allowing teams to focus on critical problems first. Distinguishes between must-fix violations and nice-to-have improvements.

### Contextual Reporting
Reports violations with surrounding code context, making it easy to locate and understand issues. Provides specific line numbers and code snippets for each finding.

## Usage

Load the agent configuration file `agent.md` in Augment Code CLI. The agent will analyze PHP files and provide detailed compliance reports with actionable recommendations.

## Workflow

The agent systematically reviews code structure, formatting, naming conventions, and architectural patterns. It generates comprehensive reports that help teams improve code quality and maintain consistency.

## Standards Coverage

Covers PSR-1 (Basic Coding Standard), PSR-12 (Extended Coding Style), PSR-4 (Autoloading), and other relevant PHP-FIG standards. Also checks for common PHP best practices and anti-patterns.

## Best Practices

The agent promotes understanding of PHP standards rather than blind compliance. It explains the reasoning behind each standard and helps developers make informed decisions about code quality.

## Technical Approach

Uses static analysis techniques to examine code structure, naming patterns, and formatting. Provides constructive feedback that balances strict standards compliance with practical development needs.

