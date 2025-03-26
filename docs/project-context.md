# Project Context

*Updated: 2024-03-21 14:30*

## Purpose

This project focuses on document template management and content processing, providing a structured approach to:
- Template creation and management
- Content ingestion and validation
- Document generation from templates
- Quality assurance and output validation

## Directory Structure

```
/docs/                 # Documentation and templates root
├── output/         # Output based on templates and any input context
│   └── [type]/        # output type based on template name (type-template.md)
├── templates/         # Document templates for specific types of output
├── working-memory/   # Active processing and tasks
│   ├── open/        # Current tasks in progress for document generation
│   └── done/        # Completed tasks with document generated output
/scripts/            # Processing and utility scripts
├── validation/     # Content validation utilities
├── generation/     # Document generation scripts
└── cleanup/        # Maintenance utilities
```

## Best Practices

1. Problem Assessment
   - Thoroughly analyze requirements before starting
   - Identify all stakeholders and their needs
   - Document assumptions and constraints
   - List potential risks and mitigation strategies

2. Clarification Process
   - Ask specific, targeted questions
   - Verify understanding through examples
   - Document all clarifications received
   - Update requirements based on responses

3. Template Management
   - Follow consistent naming conventions
   - Document template purpose and usage
   - Version control all templates
   - Maintain template changelog

4. Content Processing
   - Validate input against requirements
   - Follow defined processing workflows
   - Document any content transformations
   - Maintain audit trail of changes

5. Quality Control
   - Review generated documents against templates
   - Validate content accuracy and completeness
   - Check formatting and structure
   - Document QA results and issues

6. Documentation
   - Keep all documentation current
   - Follow standard documentation formats
   - Cross-reference related documents
   - Maintain clear audit trails
