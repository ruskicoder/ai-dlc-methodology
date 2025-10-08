# Implementation Plan

- [x] 1. Create master methodology document

  - Write AI-Driven Development Lifecycle overview with core principles (ground-truth, explicit approval, iterative refinement)
  - Document three-phase workflow (Requirements → Design → Tasks) with Mermaid state diagram
  - Include entry points (create, update, execute) and decision tree for when to use specs
  - Document all workflow constraints: explicit approval required, no automatic progression, sequential phase execution, blocking behavior without approval
  - Include troubleshooting guidance for requirements stalls, research limitations, design complexity
  - _Requirements: 1.1-1.5, 8.1-8.7, 7.1-7.10, 11.1-11.6_

- [x] 2. Create requirements phase document

  - Document EARS format (WHEN/THEN, IF/THEN, WHILE/THEN) with user story template
  - Include requirements.md structure template and file location (.kiro/specs/{feature_name}/)
  - Explain approval process with userInput tool ('spec-requirements-review' reason code)
  - Provide best practices and complete example requirements document
  - _Requirements: 2.1-2.8_

- [x] 3. Create design phase document

  - Document required sections (Overview, Architecture, Components, Data Models, Error Handling, Testing)
  - Explain research approach (in-context, no separate files) and Mermaid diagram usage
  - Include approval process with userInput tool ('spec-design-review' reason code)
  - Provide complete example design document with backward navigation guidance
  - _Requirements: 3.1-3.8, 17.1-17.7_

- [x] 4. Create tasks phase document

  - Document task format (checkbox, two-level hierarchy, decimal notation)
  - Include coding-only constraint with explicit exclusions list
  - Explain incremental building (no orphaned code) and requirement references
  - Include approval process with userInput tool ('spec-tasks-review' reason code)
  - Provide complete example task list
  - _Requirements: 4.1-4.10_

- [x] 5. Create task execution guide

  - Document pre-execution requirements (read all spec docs) and one-task-at-a-time principle
  - Explain task status management (not_started, in_progress, completed) with taskStatus tool
  - Include sub-task handling, verification process, and stop-and-review pattern
  - Provide complete execution example with status updates
  - _Requirements: 5.1-5.8, 14.1-14.7_

- [x] 6. Create steering mechanism document

  - Document three inclusion modes (always, conditional with fileMatch, manual with context key)
  - Include file reference syntax (#[[file:<relative_file_name>]]) and front-matter configuration
  - Provide use cases (team standards, OpenAPI/GraphQL integration) with example steering files

  - _Requirements: 6.1-6.7, 20.1-20.5_

- [x] 7. Create integration features document

  - Document chat context (#File, #Folder, #Problems, #Terminal, #Git, #Codebase)
  - Explain agent hooks (event-triggered and manual) with examples
  - Include MCP configuration (workspace and user level) with uvx setup and tool management
  - Document autonomy modes (Autopilot and Supervised)
  - _Requirements: 10.1-10.8, 9.1-9.6_

- [x] 8. Create tool reference document

  - Document file tools (fsWrite, fsAppend, strReplace with exact matching, deleteFile)
  - Include reading tools (readFile, readMultipleFiles), search tools (grepSearch, fileSearch)
  - Document execution (executePwsh), interaction (userInput), and task tools (taskStatus)
  - Provide tool selection guidelines (never 'cd', use file tools over CLI) and platform-specific commands
  - _Requirements: 16.1-16.10, 13.1-13.5_

- [x] 9. Create communication guide document

  - Document principles (knowledgeable not instructive, supportive not authoritative)
  - Include formatting rules (no headers unless multi-step, no bold, complete code blocks)
  - Explain workflow transparency (don't mention steps), avoiding repetition, and tone guidelines
  - Provide good vs. bad response examples
  - _Requirements: 15.1-15.10_

- [x] 10. Create security and safety guide document

  - Document refusal policies (sensitive topics, malicious code) with response templates
  - Include PII handling (substitution with placeholders) and security best practices
  - Explain internal details protection and safe code generation (syntax validation, runnable)
  - Document code generation principles: minimal code only, immediately runnable, accessibility compliant, incremental building
  - Include error handling guidance (alternative approaches after failures) and security scenario examples
  - _Requirements: 19.1-19.6, 18.1-18.6, 12.1-12.7_

- [x] 11. Create complete single-file instructions document



  - Create instructions.md containing the ENTIRE Kiro methodology in one comprehensive file for AI agents with single instruction field
  - Include complete AI-Driven Development Lifecycle workflow from initial idea to task execution
  - Document all three phases with full details: Requirements (EARS format, user stories, approval), Design (research, sections, Mermaid), Tasks (coding-only, incremental)
  - Include complete task execution workflow with all constraints (read all docs, one-at-a-time, status management, stop-and-review)
  - Document all workflow constraints and rules: explicit approval required, blocking behavior, sequential execution, no automatic progression, feedback-revision cycles
  - Document all approval mechanisms with userInput tool and three reason codes (spec-requirements-review, spec-design-review, spec-tasks-review)
  - Include complete tool reference with all constraints (fsWrite, fsAppend, strReplace exact matching, never 'cd', tool selection guidelines)
  - Document steering mechanism with three inclusion modes (always, conditional, manual) and file reference syntax (#[[file:...]])
  - Include integration features (chat context types, agent hooks, MCP configuration with workspace/user levels, autonomy modes)
  - Document communication principles (knowledgeable not instructive, supportive not authoritative, no workflow transparency, formatting rules, avoiding repetition)
  - Include security constraints (PII handling, malicious code refusal, sensitive topics, internal details protection)
  - Document code generation principles (minimal code, immediately runnable, accessibility compliant, incremental building, test-driven)
  - Include troubleshooting guidance (requirements stalls, research limitations, design complexity, repeat failures)
  - Provide workflow state diagram, data models (workflow state, task state, tool reference)
  - Include quick reference tables: EARS patterns, approval signals, tool selection decision tree, platform-specific commands, task status states
  - Document best practices for each phase and common pitfalls to avoid
  - Format with clear hierarchical sections, complete workflow steps, and actionable instructions for AI agents
  - _Requirements: All requirements 1-21 (complete methodology consolidation)_
