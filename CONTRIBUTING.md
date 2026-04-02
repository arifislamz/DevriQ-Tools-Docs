# Contributing to DevriQ-Tools-Docs

Thank you for your interest in contributing to the DevriQ Tools documentation! This guide will help you understand how to contribute effectively.

## 🎯 Ways to Contribute

### 📝 Documentation Improvements
- Improve existing guides and tutorials
- Fix typos and grammatical errors
- Add more examples and use cases
- Clarify confusing sections
- Update outdated information

### 🐛 Bug Reports
- Report documentation errors
- Flag outdated tool information
- Identify broken links
- Suggest documentation restructuring

### 💡 New Content
- Add guides for new tools
- Create workflow examples
- Write troubleshooting guides
- Contribute use case studies

### 🗣️ Community Engagement
- Answer questions in discussions
- Share your experiences
- Provide feedback on documentation
- Help other users

## 📋 Contribution Guidelines

### Before You Start
1. **Read existing documentation** to understand the style and format
2. **Check for duplicates** — ensure someone else hasn't already documented this
3. **Review the issue tracker** for planned improvements
4. **Fork and clone** the repository

### Content Standards

#### 📐 **Formatting Standards**
- Use **Markdown best practices**
- Include clear section headers with `##`, `###`, `####`
- Use code blocks with language specification
- Add internal cross-links for related content
- Include links to live tools

#### 🔗 **Linking Standards**
- **Internal links**: Use relative paths `[Guide](./docs/category/file.md)`
- **External links**: Link to `https://tools.devriq.in/tool-name/`
- **Always provide anchor text** — no bare URLs
- **Test all links** before submitting

#### ✏️ **Writing Style**
- **Clear and concise**: Avoid unnecessary jargon
- **Active voice**: "Click the button" not "The button should be clicked"
- **User-focused**: Think about your audience
- **Professional but friendly**: Balance formality with approachability
- **Examples**: Always include practical examples

#### 🎨 **Structure Template**

For tool guides, follow this structure:

```markdown
# [Tool Name]

## Overview
- What does it do?
- Key features
- Who should use it?

## How to Use
Step-by-step instructions with screenshots/examples

## Features
List of available features

## Use Cases
Real-world applications

## Tips & Tricks
Pro tips for power users

## Related Tools
Links to similar tools

## FAQ
Common questions about this tool

---
**Live Tool**: [Link to tool](https://tools.devriq.in/tool-name/)
```

### 🔄 Pull Request Process

1. **Create a branch** with a descriptive name:
   ```
   git checkout -b improve/pdf-tools-guide
   git checkout -b add/new-tool-guide
   git checkout -b fix/broken-links
   ```

2. **Make your changes** following the guidelines above

3. **Test your changes**:
   - Verify all links work
   - Check markdown formatting
   - Ensure consistency with existing docs
   - Proofread carefully

4. **Commit with clear messages**:
   ```
   git commit -m "docs: improve PDF tools guide with more examples"
   git commit -m "docs: add new AI tools documentation"
   git commit -m "fix: correct broken links in dev tools section"
   ```

5. **Push to your fork**:
   ```
   git push origin improve/pdf-tools-guide
   ```

6. **Open a Pull Request** with:
   - Clear title describing the change
   - Detailed description of what was changed and why
   - References to any related issues
   - Links to new documentation (if applicable)

7. **Respond to feedback** and make requested changes

## ✅ Quality Checklist

Before submitting a PR, verify:

- [ ] Content is accurate and up-to-date
- [ ] All links are working (internal and external)
- [ ] Markdown formatting is correct
- [ ] No spelling or grammar errors
- [ ] Consistent with existing documentation style
- [ ] Screenshots/images are clear and relevant
- [ ] Cross-links to related content are included
- [ ] Content follows the structure guidelines
- [ ] No sensitive information is exposed
- [ ] Tested in a markdown viewer

## 🚫 What NOT to Include

**For security reasons, do NOT include:**
- API keys or secrets
- Database credentials
- Server configuration details
- Internal infrastructure information
- Sensitive business logic
- Email addresses (besides public ones)
- User data or personal information

**Best practices:**
- Keep technology stack general
- Focus on user-facing features
- Explain security without exposing vulnerabilities
- Use placeholder values for examples

## 🏆 Recognition

Contributors will be:
- Recognized in the documentation
- Added to the `TEAM.md` file
- Featured in release notes (if applicable)
- Appreciated in our community

## ❓ Questions?

- 📖 Check existing documentation first
- 💬 Open a GitHub Discussion
- 📧 Contact [contact@devriq.in](mailto:contact@devriq.in)
- 🌐 Visit [devriq.in](https://devriq.in)

## 📚 Additional Resources

- [Markdown Guide](https://www.markdownguide.org/)
- [GitHub Flavored Markdown](https://github.github.com/gfm/)
- [Writing Effective Documentation](https://documentation.divio.com/)
- [Technical Writing Style Guide](https://developers.google.com/style)

---

## 📝 Code of Conduct

### Our Commitment
We are committed to providing a welcoming and inclusive environment for all contributors.

### Expected Behavior
- Be respectful and inclusive
- Provide constructive feedback
- Focus on ideas, not people
- Help others learn and grow

### Unacceptable Behavior
- Harassment or discriminatory language
- Trolling or personal attacks
- Sharing others' private information
- Any other unethical conduct

### Reporting Issues
If you experience or witness unacceptable behavior, please report it to [contact@devriq.in](mailto:contact@devriq.in).

---

**Thank you for helping make DevriQ Tools documentation better!** 🙏

Your contributions help thousands of users get the most out of our platform.
