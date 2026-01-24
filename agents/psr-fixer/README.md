# PSR Fixer

Automatic PHP Standards Recommendations compliance fixer for PHP codebases.

## Purpose

This agent automatically fixes PHP code to comply with PSR standards, particularly PSR-1 and PSR-12. It transforms non-compliant code into standards-compliant code through automated refactoring and formatting.

## Core Capabilities

- Adds strict types declarations to PHP files
- Fixes naming conventions for classes, methods, and properties
- Corrects visibility modifiers (public, protected, private)
- Ensures PSR-1 and PSR-12 compliance
- Automated code formatting and structure improvements

## Key Features

### Strict Types Enforcement
Automatically adds `declare(strict_types=1);` declarations to PHP files, ensuring type safety and preventing implicit type coercion issues.

### Naming Convention Fixes
Corrects class names to PascalCase, method names to camelCase, and ensures constants use UPPER_CASE_SNAKE_CASE formatting according to PSR standards.

### Visibility Modifiers
Ensures all class properties and methods have explicit visibility declarations (public, protected, or private), eliminating implicit public declarations.

### Code Formatting
Applies PSR-12 formatting rules including proper indentation, brace placement, spacing, and line length constraints.

## Usage

Load the agent configuration file `agent.md` in Augment Code CLI. The agent will analyze PHP code and automatically apply PSR compliance fixes while preserving functionality.

## Workflow

The agent systematically processes PHP files to identify and fix PSR violations. It prioritizes changes that improve code quality and maintainability while ensuring backward compatibility where possible.

## Standards Coverage

Focuses on PSR-1 (Basic Coding Standard) and PSR-12 (Extended Coding Style Guide) compliance. Addresses file structure, namespace declarations, class definitions, method signatures, and code formatting.

## Best Practices

The agent applies industry-standard PHP coding practices, ensuring code is consistent, readable, and maintainable. It follows the principle of making minimal necessary changes to achieve compliance while respecting existing code architecture.

## Technical Approach

Uses pattern recognition to identify PSR violations and applies targeted fixes. Maintains code functionality while improving structure and formatting. Provides clear explanations of changes made and reasons for each fix.

