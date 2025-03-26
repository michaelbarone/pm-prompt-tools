# Template Structure Guide

*Updated: 2024-03-26 16:45*

## Overview
This document defines the standard structure for all templates in the system. Each template must follow this structure to ensure consistent document generation and maintenance.

## Standard Sections

### Initial Context
- Must be completed first before any other sections
- Contains template-specific required questions
- All questions in this section must be answered before proceeding
- Forms the foundation for other sections
- May include dependencies that other sections will reference

Example structure:
```markdown
## Initial Context

### Required Information
- [Question 1]: [Answer]
- [Question 2]: [Answer]
- ...

### Quick Summary
[Template-specific summary format]
```

### Manual Entry
- Reserved for user-provided context and additional information
- Content added here may be referenced by other sections
- Should be updated as the document evolves
- Serves as a flexible space for important context not captured in other sections

Example structure:
```markdown
## Manual Entry

### Additional Context
[User-provided information that doesn't fit in other sections]

### Notes
[Important considerations or updates]
```

### Template-Specific Sections
- Each template defines its own additional sections
- May depend on information from Initial Context or Manual Entry
- Should clearly indicate any dependencies on other sections
- May include their own clarifying questions

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

## Section Dependencies

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
- ALWAYS complete Initial Context before other sections
- NEVER skip dependency checks when updating sections
- ALWAYS allow for Manual Entry updates
- NEVER remove or modify template section structure
- ALWAYS track section completion status
- ALWAYS validate dependencies before marking sections complete 