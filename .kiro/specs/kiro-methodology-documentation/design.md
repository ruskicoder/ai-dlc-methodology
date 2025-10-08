# Design Document: Kiro Spec-Driven Development Methodology Documentation

## Overview

This design outlines the structure and content for comprehensive documentation of Kiro's AI-Driven Development Lifecycle and Spec-Driven Development methodology. The documentation will be organized as a multi-document system that captures every aspect of how Kiro's agentic AI operates, from high-level methodology to granular implementation details.

The documentation system will consist of:
1. **Master Methodology Document** - Core concepts, principles, and lifecycle overview
2. **Workflow Phase Documents** - Detailed documentation for Requirements, Design, and Tasks phases
3. **Execution Guide** - Task execution workflow and constraints
4. **Integration Reference** - Steering, hooks, MCP, and context features
5. **Tool Reference** - Complete tool catalog with usage patterns and constraints
6. **Communication Guide** - Response style, tone, and interaction principles
7. **Security & Safety Guide** - Constraints, guardrails, and best practices
8. **Complete Examples** - End-to-end workflow demonstrations

This modular approach allows readers to navigate to specific topics while maintaining a cohesive understanding of the complete system.

## Architecture

### Documentation Structure

```
kiro-methodology-documentation/
├── 01-master-methodology.md          # Core methodology and lifecycle
├── 02-requirements-phase.md          # Requirements phase deep-dive
├── 03-design-phase.md                # Design phase deep-dive
├── 04-tasks-phase.md                 # Tasks phase deep-dive
├── 05-task-execution.md              # Execution workflow and constraints
├── 06-steering-mechanism.md          # Steering files and context
├── 07-integration-features.md        # Hooks, MCP, chat context
├── 08-tool-reference.md              # Complete tool catalog
├── 09-communication-guide.md         # Response style and principles
├── 10-security-safety.md             # Security constraints and guardrails
├── 11-workflow-examples.md           # Complete end-to-end examples
└── 12-quick-reference.md             # Cheat sheet and quick lookup
```

### Content Organization Principles

1. **Progressive Disclosure**: Start with high-level concepts, drill down to specifics
2. **Cross-Referencing**: Link related concepts across documents
3. **Practical Examples**: Include code snippets, file examples, and real scenarios
4. **Visual Aids**: Use Mermaid diagrams for workflows, state machines, and architecture
5. **Searchability**: Use consistent terminology and clear section headers
6. **Completeness**: Every constraint, rule, and behavior must be documented

## Components and Interfaces

### 1. Master Methodology Document

**Purpose**: Provide comprehensive overview of Kiro's spec-driven development approach

**Key Sections**:
- Introduction to AI-Driven Development Lifecycle
- Core Principles (ground-truth establishment, explicit approval, iterative refinement)
- Three-Phase Workflow Overview (Requirements → Design → Tasks)
- Entry Points and State Management
- Workflow State Diagram (Mermaid)
- When to Use Specs vs. Direct Implementation
- Benefits and Trade-offs

**Content Requirements**:
- Explain the philosophy behind spec-driven development
- Document the principle of establishing ground-truths with user approval
- Describe the iterative nature and feedback loops
- Include the complete workflow state diagram
- Provide decision tree for when to create specs
- Address Requirements 1, 8, 9

### 2. Requirements Phase Document

**Purpose**: Complete guide to transforming ideas into structured requirements

**Key Sections**:
- Phase Overview and Objectives
- EARS Format Specification (WHEN/THEN, IF/THEN, WHILE/THEN patterns)
- User Story Format ("As a [role], I want [feature], so that [benefit]")
- Document Structure and Template
- File Location and Naming (.kiro/specs/{feature_name}/requirements.md)
- Review and Approval Process
- UserInput Tool Usage (spec-requirements-review)
- Iteration and Modification Workflow
- Best Practices for Writing Requirements
- Common Pitfalls and How to Avoid Them
- Example Requirements Document (complete, realistic)

**Content Requirements**:
- Provide complete EARS syntax reference with examples
- Include template for requirements.md structure
- Document exact approval workflow with tool usage
- Show multiple examples of well-formed requirements
- Explain how to handle edge cases and constraints
- Address Requirement 2

### 3. Design Phase Document

**Purpose**: Guide for creating comprehensive technical designs from requirements

**Key Sections**:
- Phase Overview and Objectives
- Research and Context Building Approach
- Required Design Sections:
  - Overview
  - Architecture
  - Components and Interfaces
  - Data Models
  - Error Handling
  - Testing Strategy
- File Location and Naming (.kiro/specs/{feature_name}/design.md)
- Mermaid Diagram Usage
- Research Integration (in-context, no separate files)
- Review and Approval Process
- UserInput Tool Usage (spec-design-review)
- Backward Navigation to Requirements
- Design Decision Documentation
- Example Design Document (complete, realistic)

**Content Requirements**:
- Provide template for design.md structure
- Include examples of each required section
- Show Mermaid diagram examples (architecture, sequence, state)
- Document research workflow and integration
- Explain how design addresses requirements
- Address Requirement 3, 17

### 4. Tasks Phase Document

**Purpose**: Guide for converting designs into actionable implementation plans

**Key Sections**:
- Phase Overview and Objectives
- Task List Format (checkbox, two-level hierarchy)
- Task Numbering Convention (decimal notation: 1.1, 1.2)
- Task Content Requirements:
  - Clear objective
  - Sub-bullets with details
  - Requirement references
- Coding-Only Constraint (explicit exclusions list)
- Actionability Criteria
- Incremental Building Principle (no orphaned code)
- File Location and Naming (.kiro/specs/{feature_name}/tasks.md)
- Review and Approval Process
- UserInput Tool Usage (spec-tasks-review)
- Separation from Implementation
- Example Task List (complete, realistic)

**Content Requirements**:
- Provide template for tasks.md structure
- List all excluded non-coding activities
- Show examples of well-formed tasks
- Demonstrate requirement referencing
- Explain incremental building approach
- Address Requirement 4

### 5. Task Execution Guide

**Purpose**: Complete reference for executing tasks during implementation

**Key Sections**:
- Execution Workflow Overview
- Pre-Execution Requirements (read all spec docs)
- Task Selection and Sub-Task Handling
- One-Task-at-a-Time Principle
- Task Status Management:
  - not_started state
  - in_progress state
  - completed state
- TaskStatus Tool Usage
- Verification Against Requirements
- Stop-and-Review Pattern
- Task Recommendations
- Distinguishing Questions from Execution Requests
- Example Execution Session

**Content Requirements**:
- Document complete execution workflow
- Provide taskStatus tool examples
- Show task selection logic
- Demonstrate verification process
- Include complete execution example
- Address Requirements 5, 14

### 6. Steering Mechanism Document

**Purpose**: Complete guide to steering files and context injection

**Key Sections**:
- Steering Concept and Purpose
- File Location (.kiro/steering/*.md)
- Three Inclusion Modes:
  - Always Included (default)
  - Conditional (fileMatch with front-matter)
  - Manual (context key '#')
- Front-Matter Configuration
- File Reference Syntax (#[[file:<relative_file_name>]])
- Use Cases:
  - Team standards and norms
  - Project information
  - Build/test instructions
  - OpenAPI/GraphQL spec integration
- Creating and Updating Steering Files
- Example Steering Files

**Content Requirements**:
- Provide steering file templates
- Show front-matter examples
- Demonstrate file reference syntax
- Include realistic use case examples
- Document OpenAPI/GraphQL integration
- Address Requirements 6, 20

### 7. Integration Features Document

**Purpose**: Reference for all Kiro integration capabilities

**Key Sections**:
- Chat Context Features:
  - #File
  - #Folder
  - #Problems
  - #Terminal
  - #Git
  - #Codebase
- Agent Hooks:
  - Event-triggered hooks
  - Manual hooks
  - Hook creation and management
  - Example hooks (test updates, translations, spell-check)
- Model Context Protocol (MCP):
  - Configuration files (workspace and user level)
  - Server setup
  - Tool auto-approval
  - Disabled tools management
  - Example MCP configurations
- Autonomy Modes:
  - Autopilot mode
  - Supervised mode

**Content Requirements**:
- Document each context type with examples
- Provide hook creation guide
- Include complete MCP configuration reference
- Show autonomy mode differences
- Address Requirements 9, 10

### 8. Tool Reference Document

**Purpose**: Complete catalog of all tools with usage patterns and constraints

**Key Sections**:
- File Operation Tools:
  - fsWrite (create/overwrite)
  - fsAppend (add content)
  - strReplace (edit existing content)
  - deleteFile
- File Reading Tools:
  - readFile
  - readMultipleFiles
- Search Tools:
  - grepSearch (content search)
  - fileSearch (filename search)
- Directory Tools:
  - listDirectory
- Execution Tools:
  - executePwsh
- User Interaction Tools:
  - userInput (with reason codes)
- Task Management Tools:
  - taskStatus
- Tool Selection Guidelines
- Platform-Specific Considerations
- Common Patterns and Anti-Patterns

**Content Requirements**:
- Document each tool with parameters and examples
- Explain tool selection logic
- Show common usage patterns
- List anti-patterns (e.g., never use 'cd')
- Include platform-specific command examples
- Address Requirements 13, 16

### 9. Communication Guide Document

**Purpose**: Reference for Kiro's response style and interaction principles

**Key Sections**:
- Core Communication Principles:
  - Knowledgeable, not instructive
  - Supportive, not authoritative
  - Easygoing, not mellow
- Tone and Personality
- Language Style (speak like a dev when necessary)
- Formatting Rules:
  - No markdown headers (unless multi-step)
  - No bold text
  - Use bullet points for readability
  - Complete code blocks
- Conciseness and Clarity
- Avoiding Repetition
- Workflow Transparency (don't mention steps)
- Execution Log Handling
- Code Presentation Standards
- Example Interactions

**Content Requirements**:
- Provide tone guidelines with examples
- Show good vs. bad response examples
- Document formatting rules
- Include interaction examples
- Address Requirement 15

### 10. Security and Safety Guide Document

**Purpose**: Complete reference for security constraints and guardrails

**Key Sections**:
- Sensitive Topic Refusal
- Malicious Code Prohibition
- PII Handling (substitution with placeholders)
- Security Best Practices Prioritization
- Internal Details Protection
- Cloud Implementation Discussion Restrictions
- Safe Code Generation Principles
- Error Handling and Validation
- Example Security Scenarios

**Content Requirements**:
- Document each constraint with examples
- Provide PII substitution examples
- Show refusal response templates
- Include security best practices
- Address Requirements 18, 19

### 11. Workflow Examples Document

**Purpose**: Complete end-to-end demonstrations of spec-driven development

**Key Sections**:
- Example 1: Simple Feature (User Authentication)
  - Initial idea
  - Complete requirements.md
  - User feedback and iteration
  - Complete design.md
  - User feedback and iteration
  - Complete tasks.md
  - User feedback and iteration
  - Task execution session
  - Status updates
- Example 2: Complex Feature (Multi-step Workflow)
  - Shows backward navigation
  - Shows research integration
  - Shows design complexity handling
- Example 3: Integration Feature (API Client)
  - Shows OpenAPI spec reference
  - Shows steering file usage
  - Shows MCP integration
- Annotated Walkthroughs

**Content Requirements**:
- Provide complete, realistic examples
- Show all approval points
- Include user feedback and agent responses
- Demonstrate tool usage
- Show status management
- Address Requirement 21

### 12. Quick Reference Document

**Purpose**: Cheat sheet for quick lookup of common patterns

**Key Sections**:
- Workflow Phase Checklist
- EARS Format Quick Reference
- Tool Selection Decision Tree
- UserInput Reason Codes
- Task Status States
- File Reference Syntax
- Common Commands by Platform
- Approval Signal Examples
- Troubleshooting Quick Fixes

**Content Requirements**:
- Provide condensed, scannable format
- Use tables and lists
- Include decision trees
- Cross-reference detailed docs
- Address all requirements (summary)

## Data Models

### Documentation Metadata

```typescript
interface DocumentMetadata {
  title: string;
  version: string;
  lastUpdated: Date;
  requirements: string[];  // Requirement IDs addressed
  relatedDocs: string[];   // Cross-references
}
```

### Workflow State Model

```typescript
enum WorkflowPhase {
  REQUIREMENTS = "requirements",
  DESIGN = "design",
  TASKS = "tasks",
  EXECUTION = "execution"
}

interface WorkflowState {
  currentPhase: WorkflowPhase;
  requirementsApproved: boolean;
  designApproved: boolean;
  tasksApproved: boolean;
  featureName: string;
  specDirectory: string;
}
```

### Task State Model

```typescript
enum TaskStatus {
  NOT_STARTED = "not_started",
  IN_PROGRESS = "in_progress",
  COMPLETED = "completed"
}

interface Task {
  id: string;           // e.g., "1.1", "2.3"
  description: string;
  details: string[];
  requirements: string[];
  status: TaskStatus;
  parentTask?: string;
  subTasks?: string[];
}
```

### Tool Reference Model

```typescript
interface Tool {
  name: string;
  category: "file" | "search" | "execution" | "interaction" | "task";
  parameters: Parameter[];
  constraints: string[];
  examples: Example[];
  platformSpecific: boolean;
}

interface Parameter {
  name: string;
  type: string;
  required: boolean;
  description: string;
}

interface Example {
  scenario: string;
  code: string;
  explanation: string;
}
```

## Error Handling

### Documentation Completeness Validation

- Each document must address specific requirements (tracked via metadata)
- Cross-references must be valid (link to existing sections)
- Examples must be complete and runnable
- Mermaid diagrams must render correctly

### Content Quality Checks

- EARS format validation for requirement examples
- Code snippet syntax validation
- Tool parameter accuracy verification
- Consistency checks across documents (terminology, formatting)

### User Feedback Integration

- Track common questions and add clarifications
- Identify gaps through usage patterns
- Iterate on examples based on user confusion
- Add troubleshooting sections for common issues

## Testing Strategy

### Documentation Review Process

1. **Completeness Review**: Verify all 21 requirements are addressed
2. **Accuracy Review**: Validate against actual Kiro behavior
3. **Clarity Review**: Ensure explanations are understandable
4. **Example Validation**: Test all code snippets and examples
5. **Cross-Reference Check**: Verify all links and references
6. **Consistency Check**: Ensure terminology and formatting consistency

### Validation Criteria

- Each requirement has corresponding design sections
- All constraints from requirements are documented
- Examples cover common and edge cases
- Diagrams accurately represent workflows
- Tool documentation matches actual tool behavior
- Security constraints are clearly stated

### User Testing Approach

- Provide documentation to new Kiro users
- Collect feedback on clarity and completeness
- Identify missing information or confusing sections
- Iterate based on real-world usage
- Track frequently asked questions

### Maintenance Strategy

- Update documentation when Kiro behavior changes
- Add new examples based on user requests
- Expand troubleshooting sections based on issues
- Keep tool reference synchronized with actual tools
- Version documentation alongside Kiro releases

## Implementation Notes

### Writing Style Guidelines

- Use active voice
- Keep sentences concise
- Provide context before details
- Use examples liberally
- Explain "why" not just "what"
- Include visual aids (diagrams, tables)
- Use consistent terminology
- Cross-reference related concepts

### Diagram Standards

- Use Mermaid for all diagrams
- Include diagram source in markdown
- Provide text descriptions for accessibility
- Keep diagrams focused (one concept per diagram)
- Use consistent styling and colors

### Example Standards

- Examples must be complete and realistic
- Include context (what problem it solves)
- Show both good and bad patterns
- Annotate complex examples
- Test all code snippets
- Use placeholder data (no real PII)

### Cross-Referencing Strategy

- Link to related sections within documents
- Link to other documents for deep dives
- Use consistent link text
- Provide context for links
- Avoid circular references
- Create index/glossary for key terms
