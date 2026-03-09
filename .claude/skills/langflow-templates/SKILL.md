# langflow-templates Development Patterns

> Auto-generated skill from repository analysis

## Overview

This codebase manages a collection of Langflow templates organized into business functions and AI patterns. The repository contains JSON configuration files that define workflow automation templates for various business use cases, from marketing automation to document intelligence. The project follows a hierarchical structure with templates categorized by their functional domain and specific use cases.

## Coding Conventions

### File Naming
- Use `snake_case` for all file and directory names
- Template files follow pattern: `template_name.json`
- Directory structure: `category/subcategory/template_name.json`

### Directory Structure
```
business_funcions/
├── sales_marketing_automation/
│   ├── marketing_content_creation/
│   │   └── template_name.json
│   └── .DS_Store
ai_patterns/
├── document_intelligence/
│   └── template_name.json
├── web_&_workflow_automation/
│   └── template_name.json
└── .DS_Store
```

### Template Format
- All templates are JSON configuration files
- Supporting documentation may include PDF files
- Each directory maintains `.DS_Store` files for macOS compatibility

### Import/Export Style
- Mixed import styles (both ES6 and CommonJS patterns detected)
- Mixed export styles depending on template requirements

## Workflows

### Add New Business Template
**Trigger:** When someone wants to create a new business automation template
**Command:** `/new-business-template`

1. Identify the appropriate business function category under `business_funcions/`
2. Navigate to the relevant subdirectory (e.g., `sales_marketing_automation/`)
3. Create a new JSON template file using `snake_case` naming
4. Update the `.DS_Store` file in the parent directory
5. Add any supporting files (PDFs, additional configs) if needed
6. Commit with descriptive message following `feat: description` pattern

**Example:**
```json
{
  "name": "email_campaign_template",
  "description": "Automated email marketing workflow",
  "components": [...],
  "connections": [...]
}
```

### Add AI Pattern Template
**Trigger:** When someone wants to create a new AI pattern template
**Command:** `/new-ai-pattern`

1. Choose the appropriate AI pattern category (`document_intelligence`, `web_&_workflow_automation`, etc.)
2. Create JSON template file in the selected `ai_patterns/` subdirectory
3. Update `.DS_Store` files for directory structure maintenance
4. Ensure template follows AI workflow patterns and component structure
5. Commit changes with descriptive message

**Example Structure:**
```
ai_patterns/document_intelligence/pdf_analyzer.json
ai_patterns/web_&_workflow_automation/web_scraper.json
```

### Update Marketing Content Templates
**Trigger:** When someone wants to modify marketing automation flows
**Command:** `/update-marketing-template`

1. Navigate to `business_funcions/sales_marketing_automation/marketing_content_creation/`
2. Locate the existing template JSON file to modify
3. Update template configuration maintaining JSON structure
4. Update `.DS_Store` file if directory structure changed
5. Test template configuration if possible
6. Commit with clear description of changes made

### Batch Template Addition
**Trigger:** When someone wants to add several related templates at once
**Command:** `/batch-add-templates`

1. Plan template organization across multiple categories
2. Create JSON templates in their respective directories:
   - Business functions under `business_funcions/`
   - AI patterns under `ai_patterns/`
3. Update all relevant `.DS_Store` files
4. Ensure consistent naming and structure across all templates
5. Group related templates logically
6. Commit all templates together with comprehensive message

### Update Existing Template
**Trigger:** When someone wants to update or fix an existing template
**Command:** `/update-template`

1. Locate the existing template JSON file
2. Make necessary modifications to the template configuration
3. Validate JSON structure and syntax
4. Update `.DS_Store` files if needed
5. Test template functionality if possible
6. Commit with specific description of what was updated

## Testing Patterns

- Test files follow `*.test.*` pattern
- Testing framework not clearly defined in repository
- Manual testing likely involves importing templates into Langflow
- Validation focuses on JSON structure and template functionality
- Consider testing template imports and workflow execution

## Commit Conventions

- Use freeform commit messages with `feat:` prefix for new features
- Keep commit messages concise (average 43 characters)
- Focus on describing what template or functionality was added/modified
- Example: `feat: add customer segmentation template`

## Commands

| Command | Purpose |
|---------|---------|
| `/new-business-template` | Add a new business function automation template |
| `/new-ai-pattern` | Add a new AI pattern template for document intelligence or workflow automation |
| `/update-marketing-template` | Update or modify marketing content creation templates |
| `/batch-add-templates` | Add multiple related templates across different categories |
| `/update-template` | Modify an existing template configuration |