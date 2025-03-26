# pm-prompt-tools

*Updated: 2025-03-26 12:17*

A collection of tools and utilities for managing and working with AI prompts in development environments. This project focuses on standardizing prompt management, rule creation, and documentation practices.

## Features

- 📝 **Documentation Standards**: Consistent formatting and organization of documentation
- 🔧 **Rule Management**: Structured system for creating and maintaining AI prompt rules

## Directory Structure

```
.cursor/
└── rules/                # AI prompt rules and guidelines
docs/
├── templates/            # Document templates
├── output/               # Generated documentation
cursor-settings.md        # IDE settings and configurations
README.md                 # this file
```

## Project Init

### Cursor/IDE setup

Copy the section of `cursor-setting.md` into your cursor settings User Rules section and customize as needed

NOTE: to prevent cursor IDE from changing or possibly disabling triggers of rules, update your user settings .json file with this to disable the built in mdc editor:
JSON Configuration:

```json
    "workbench.editorAssociations": {
        "*.mdc": "default"
    }
```

After disabling the editer, continue to add/update rules in the .cursor/rules directory.

## Usage

### 📝 Document Management

The document creation process is template-driven, where each template defines its own context and requirements.

#### Process Overview

1. Templates (`docs/templates/`)
   - Each template follows format: `[type]-template.md`
   - Template defines required sections and context
   - Review `template-structure.md` for template creation
     - Create new template types as needed for new document structures

2. Document Creation

   ```shell
   "Create a new [type] of document"
   ```

   - AI will:
     - Load appropriate template
     - Guide you through required sections
     - Generate output in `docs/output/`

3. Document Updates

   ```shell
   "Update [type] document: [name]"
   ```

   - AI will:
     - Load existing document
     - Apply template rules
     - Help modify content while maintaining structure

### 🔧 Rule Management

1. **Rule Creation and Management**: Follow the standards in `.cursor/rules/` for creating new prompt rules
   - Leverage the AI to help refine rules and guidance for template use, automated reponses and prompint and other areas we want to add consistency to this project

## Contributing

Follow the established rule naming conventions and documentation standards when contributing new features or updates.
