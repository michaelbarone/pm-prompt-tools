# Template Structure Guide

*Updated: 2024-03-26 16:45*

## Overview

This document defines the standard structure for all templates in the system. Each template must follow this structure to ensure consistent document generation and maintenance.

## Standard Sections

### Initial Prompt

- Must be completed first before any other sections, the AI will prompt for these answers before creating the document
- Contains template-specific required questions
- All questions in this section must be answered before proceeding
- Forms the foundation for other sections
- May include dependencies that other sections will reference

Example structure:

```markdown
## Initial Prompt

### Required prompt title 1
<!-- commented description for prompt 1 -->
- [Question 1]: [Answer]
- ...

### Required prompt title 2
<!-- commented description for prompt 2 -->
- [Question 2]: [Answer]
- ...
```

### Rest of Template

- contains all other sections of the document template.

Example structure:

```markdown
## [Section Name]

### Dependencies
- Requires [specific information] from Initial Context
- May reference [specific aspects] from Manual Entry

### Section Content
[Template-specific content structure]

### Clarifying Questions
[Questions needed to complete this section]
```

## Section Dependencies (if needed)

### Dependency Types

1. **Direct Dependencies**
   - Section explicitly requires information from another section
   - Must be clearly marked at the start of the section
   - Example: "Depends on: Initial Context > Project Timeline"

2. **Implicit Dependencies**
   - Section may be influenced by information in another section
   - Should be noted as "May reference: [Section > Subsection]"
   - Example: "May reference: Manual Entry > Technical Constraints"

### Handling Dependencies

- Sections with direct dependencies cannot be completed until dependencies are satisfied
- Implicit dependencies should be reviewed before section completion
- Dependencies should be documented at the section level
- Changes to referenced sections should trigger review of dependent sections

## Usage Guidelines

### Document Creation Flow

1. Complete Initial Context first
2. Allow for Manual Entry additions
3. Process other sections based on dependency order
4. Mark sections as complete only when all dependencies are satisfied

### Section Status Tracking

```markdown
[✓] Complete - All required information provided
[?] Awaiting Input - Missing required information
[!] Dependency Blocked - Waiting for other sections
[ ] Not Started - Section not yet addressed
```

### Updating Existing Documents

1. Review existing content
2. Identify affected dependencies
3. Update sections in dependency order
4. Validate all dependent sections after changes

## Critical Rules

- ALWAYS complete Initial Prompt before other sections
- NEVER skip dependency checks when updating sections
- ALWAYS allow for Manual Entry updates
- NEVER remove or modify template section structure
- ALWAYS track section completion status
- ALWAYS validate dependencies before marking sections complete

---
<!-- For AI Remove this section when using the template -->
## Template Usage Notes
1. Replace all text in [brackets] with your specific content
2. Select options by changing [ ] to [X] for your choice
3. Delete any sections that are not applicable
4. Be specific and quantitative where possible
5. Update the timestamp at the top when saving changes