# Contributing to Sample Playbooks

Thank you for your interest in contributing to this playbook repository! This document provides guidelines for creating and maintaining playbooks.

## How to Contribute

### Creating a New Playbook

1. **Check for existing playbooks** - Review the repository to avoid duplicates
2. **Use the template** - Start with [playbook-template.md](playbooks/templates/playbook-template.md)
3. **Choose the right category** - Place your playbook in the appropriate directory:
   - `incident-response/` - For security incidents, outages, and emergency responses
   - `operations/` - For routine operational tasks and maintenance
   - `security/` - For security procedures and access management
4. **Follow the naming convention** - Use lowercase with hyphens: `my-playbook-name.md`
5. **Complete all sections** - Don't leave template sections empty
6. **Submit a pull request** - Include a clear description of what the playbook covers

### Updating an Existing Playbook

1. **Make focused changes** - Update only what needs to change
2. **Update the changelog** - Add an entry with date, author, and description of changes
3. **Test if possible** - Verify procedures still work in a non-production environment
4. **Document breaking changes** - Clearly note if changes affect how the playbook is used
5. **Submit a pull request** - Explain why the update is needed

## Playbook Writing Guidelines

### Structure

Every playbook must include these sections:
- **Overview** - Brief description and when to use this playbook
- **Prerequisites** - What's needed before starting
- **Scope** - What is and isn't covered
- **Roles and Responsibilities** - Who does what
- **Procedure** - Step-by-step instructions
- **Verification** - How to confirm success
- **Rollback Procedure** - What to do if something goes wrong
- **Post-Execution** - Follow-up tasks
- **Related Resources** - Links to documentation
- **Changelog** - Version history

### Writing Style

- **Be specific**: Include exact commands, not just descriptions
- **Be clear**: Use simple, direct language
- **Be complete**: Don't assume knowledge - explain each step
- **Be actionable**: Every step should have clear actions to take
- **Use active voice**: "Run the command" not "The command should be run"
- **Include expected outcomes**: Tell users what should happen after each step

### Format Guidelines

#### Commands and Code
Use code blocks for commands:
```bash
# Example command
sudo systemctl restart service-name
```

#### Lists and Steps
Number action items within each step:
```markdown
**Action items:**
1. First action
2. Second action
3. Third action
```

#### Links
Use descriptive link text:
```markdown
- [System Architecture Diagram] - Good
- [Click here] - Bad
```

#### Examples
Include concrete examples where helpful:
```markdown
**Example:**
If the database name is "production_db", run:
`pg_dump production_db > backup_$(date +%Y%m%d).sql`
```

## Quality Standards

### Before Submitting

Ensure your playbook:
- [ ] Uses the standard template structure
- [ ] Contains specific, actionable steps
- [ ] Includes verification procedures
- [ ] Has a rollback plan
- [ ] Documents prerequisites clearly
- [ ] Uses proper Markdown formatting
- [ ] Contains no sensitive information (passwords, keys, internal IPs)
- [ ] Has been reviewed for clarity
- [ ] Includes expected outcomes for major steps
- [ ] Links to related resources

### Review Process

1. **Submission** - Create a pull request with your playbook
2. **Automated checks** - Markdown formatting will be validated
3. **Peer review** - At least one reviewer will check for:
   - Completeness and accuracy
   - Clarity and usability
   - Adherence to guidelines
   - Security considerations
4. **Revisions** - Address any feedback from reviewers
5. **Merge** - Once approved, your playbook will be merged

## Maintenance

### Regular Updates

Playbooks should be reviewed and updated:
- When underlying systems or procedures change
- After each execution (note any issues)
- At least annually for accuracy
- When team feedback suggests improvements

### Deprecation

When a playbook is no longer needed:
1. Add a deprecation notice at the top
2. Link to the replacement playbook if applicable
3. Keep the playbook for historical reference (don't delete)
4. Remove from the main README list

## Security Considerations

- **Never include sensitive data**: No passwords, API keys, or secrets
- **Use placeholders**: `<username>`, `<api-key>`, `<server-address>`
- **Reference credential stores**: Link to password managers or secret stores
- **Review for exposure**: Consider what information could help an attacker
- **Sanitize examples**: Use example.com, fictional names, dummy data

## Questions or Help

If you have questions about contributing:
- Open an issue for discussion
- Review existing playbooks for examples
- Contact the repository maintainers

## Code of Conduct

- Be respectful and professional
- Focus on constructive feedback
- Assume good intentions
- Help others learn and improve

Thank you for helping make these playbooks better!
