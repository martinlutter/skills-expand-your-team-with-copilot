# Issue Templates

This directory contains GitHub issue form templates designed specifically for teachers and staff at Mergington High School who need to request changes to the activities website.

## Available Templates

| Template | Purpose | File |
|----------|---------|------|
| 🐛 **Bug Report** | Report problems or issues | `bug_report.yml` |
| ✨ **Feature Request** | Suggest new features | `feature_request.yml` |
| 📚 **Activity Change** | Add/update/remove activities | `activity_change.yml` |
| 🎨 **UI Improvement** | Design and UX improvements | `ui_improvement.yml` |
| 💬 **General Request** | Other types of requests | `general_request.yml` |

## Template Design

Each template is designed to:

1. **Use Simple Language**: No technical jargon or coding terms
2. **Provide Clear Examples**: Placeholder text shows exactly what to write
3. **Require Key Information**: Forces inclusion of:
   - Clear problem description
   - Acceptance criteria (how to verify completion)
   - Context and background
   - Constraints and limitations
4. **Guide With Structure**: Dropdown menus and required fields prevent incomplete submissions
5. **Be Copilot-Friendly**: Structured so GitHub Copilot can implement without clarification

## Template Structure

All issue form templates follow this pattern:

```yaml
name: Template Name
description: Brief description
title: "[Prefix]: "
labels: ["label1", "label2"]
body:
  - type: markdown
    attributes:
      value: |
        Helpful introduction text
  
  - type: textarea/dropdown/input
    id: field-id
    attributes:
      label: User-friendly question
      description: Additional context
      placeholder: "Example: Concrete example of what to write"
    validations:
      required: true/false
```

## Customization

To modify templates:

1. Edit the `.yml` files directly
2. Test locally by creating an issue
3. Ensure all required fields remain required
4. Keep examples concrete and relevant
5. Maintain non-technical language

## Configuration

`config.yml` controls:
- Whether blank issues are allowed (currently: yes)
- Contact links shown in the issue chooser
- Links to documentation and help resources

## Testing Templates

Templates are automatically validated for:
- Valid YAML syntax
- Required fields present
- Acceptance criteria included
- Helpful examples provided
- Appropriate field validations

## For Developers

When receiving issues from these templates:

1. **All Required Context Is Present**: Teachers are prompted for everything needed
2. **Acceptance Criteria Defined**: Clear definition of "done"
3. **Examples Provided**: Context helps understand the request
4. **Structured Data**: Dropdown selections help with categorization and automation

## Resources

- [GitHub Issue Forms Documentation](https://docs.github.com/en/communities/using-templates-to-encourage-useful-issues-and-pull-requests/syntax-for-issue-forms)
- [How to Submit Issues Guide](../../docs/how-to-submit-issues.md) - For teachers
- [Development Guide](../../docs/how-to-develop.md) - For developers
