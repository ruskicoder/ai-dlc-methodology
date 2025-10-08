# Kiro AI-Driven Development Lifecycle (AI-DLC) Methodology

Complete documentation of Kiro's Spec-Driven Development methodology for autonomous AI agents. This repository contains comprehensive guides, workflows, and best practices for building software features using structured, human-supervised AI development.

## Overview

The AI-Driven Development Lifecycle (AI-DLC) is a structured approach to autonomous software development that maintains human oversight through explicit approval gates. It enables AI agents to transform rough feature ideas into production-ready implementations while ensuring developers remain in control at every critical decision point.

## Core Principles

1. **Ground-Truth Establishment** - Each phase produces a document that serves as the definitive source of truth
2. **Explicit Approval Gates** - Agent must receive clear approval before transitioning between phases
3. **Iterative Refinement** - Feedback-revision cycles continue until developer satisfaction

## Three-Phase Workflow

### Phase 1: Requirements
Transform initial concepts into structured requirements using EARS format (Easy Approach to Requirements Syntax) and user stories.

### Phase 2: Design
Create comprehensive technical designs with architecture, components, data models, error handling, and testing strategies.

### Phase 3: Tasks
Convert designs into actionable, agent-executable implementation plans with discrete coding tasks.

### Execution
Implement tasks one at a time with mandatory stop-and-review after each completion.

## Repository Structure

### Single-File Reference
- **`instructions.md`** - Complete methodology in one comprehensive file (1,352 lines) for AI agents

### Detailed Documentation
Individual guides covering specific aspects of the methodology:

1. **`01-master-methodology.md`** - Core concepts, principles, and lifecycle overview
2. **`02-requirements-phase.md`** - EARS format, user stories, and requirements workflow
3. **`03-design-phase.md`** - Design sections, research approach, and Mermaid diagrams
4. **`04-tasks-phase.md`** - Task formatting, coding-only constraints, and incremental building
5. **`05-task-execution.md`** - Execution workflow, status management, and verification
6. **`06-steering-mechanism.md`** - Steering files, inclusion modes, and file references
7. **`07-integration-features.md`** - Chat context, agent hooks, and MCP integration
8. **`08-tool-reference.md`** - Complete tool catalog with usage patterns and constraints
9. **`09-communication-guide.md`** - Response style, tone, and interaction principles
10. **`10-security-safety.md`** - Security constraints, PII handling, and safe code generation

### Spec Files
The `.kiro/specs/kiro-methodology-documentation/` directory contains the spec-driven development artifacts used to create this documentation:
- `requirements.md` - 21 detailed requirements with EARS-format acceptance criteria
- `design.md` - Technical design for the documentation system
- `tasks.md` - Implementation task list with 11 tasks

## Quick Start

### For AI Agents
Use `instructions.md` as a single comprehensive reference containing the complete methodology.

### For Developers
Start with `01-master-methodology.md` for an overview, then explore specific phase documents as needed.

### For Implementation
Follow the three-phase workflow:
1. Create requirements using EARS format
2. Design the technical solution
3. Break down into actionable tasks
4. Execute tasks one at a time with review gates

## Key Features

### Workflow Management
- Sequential phase execution with explicit approval requirements
- No automatic progression between phases or tasks
- Backward navigation supported when gaps are identified
- One-task-at-a-time execution principle

### Tool Integration
- Complete tool reference for file operations, search, execution, and interaction
- Platform-specific command guidelines (Windows/Linux/Mac)
- Critical constraints (never use 'cd', prefer file tools over CLI)

### Steering Mechanism
- Three inclusion modes: always, conditional (fileMatch), manual
- File reference syntax for including OpenAPI specs, GraphQL schemas
- Team standards and project-specific guidelines

### Security & Safety
- PII substitution requirements
- Refusal policies for malicious code and sensitive topics
- Security best practices for authentication, validation, and data protection
- Safe code generation principles (minimal, runnable, accessible)

## Communication Principles

- **Knowledgeable, not instructive** - Show expertise without being preachy
- **Supportive, not authoritative** - Enhance developer ability rather than commanding
- **Decisive, precise, and clear** - Prioritize actionable information
- **Workflow transparency** - Don't mention internal workflow steps to users

## Use Cases

### When to Use Spec-Driven Development
- Complex features with multiple components
- Unclear requirements needing structured clarification
- Design decisions requiring careful consideration
- Implementation spanning multiple sessions
- Need for traceability from requirements to code

### When to Use Direct Implementation
- Simple, well-understood changes
- Crystal clear requirements
- Straightforward single-file modifications
- Quick iteration more valuable than documentation

## Contributing

This repository documents the Kiro AI-DLC methodology. For questions, improvements, or discussions about the methodology, please refer to the comprehensive documentation provided.

## License

[Add appropriate license information]

## Related Resources

- Kiro IDE: [Add link if applicable]
- EARS Format Reference: Easy Approach to Requirements Syntax
- Mermaid Diagrams: https://mermaid.js.org/

---

**Version**: 1.0  
**Last Updated**: 2025-10-08  
**Total Documentation**: 1,352 lines (single file) + 10 detailed guides
