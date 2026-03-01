# Contributing to AI Ethics Enforcement Toolkit

**Credits:** [FutureTranz-Inc](https://github.com/FutureTranz-Inc) | [victorjquinones](https://github.com/victorjquinones)

Thank you for your interest in contributing to the AI Ethics Enforcement Toolkit! We welcome contributions from everyone. By participating in this project, you agree to abide by our [Code of Conduct](CODE_OF_CONDUCT.md).

## How to Contribute

### Reporting Bugs

- Use the [Bug Report template](.github/ISSUE_TEMPLATE/bug-report.md) when creating issues
- Include as much detail as possible
- Provide steps to reproduce the issue
- Include your environment details

### Suggesting Features

- Use the [Feature Request template](.github/ISSUE_TEMPLATE/feature-request.md)
- Clearly describe the problem you're solving
- Explain why this feature would be useful
- Consider alternative solutions

### Contributing Code

1. **Fork the repository** on GitHub
2. **Clone your fork** locally
3. **Create a feature branch** from `main`
4. **Make your changes**
5. **Test your changes** thoroughly
6. **Commit your changes** with clear, descriptive messages
7. **Push to your fork**
8. **Create a Pull Request** using the [PR template](.github/PULL_REQUEST_TEMPLATE.md)

### Commit Guidelines

- Use clear, descriptive commit messages
- Start with a verb (Add, Fix, Update, etc.)
- Keep the first line under 50 characters
- Reference issues with `#issue_number`
- **Important**: Do not include AI attribution in commits. See [AI Attribution Policy](AI_ATTRIBUTION_POLICY.md)

### Pull Request Process

1. Ensure your PR follows the template
2. Update documentation if needed
3. For AI feature work, include a PRD with `## AI Ethics & Risk` and add `ethics-checklist.yml` at repository root
4. Start from `docs/prd/PRD_TEMPLATE.md` and `docs/prd/ethics-checklist-template.yml` to satisfy required checks
5. Add tests for new features
6. Ensure all CI checks pass
7. Request review from maintainers

## Development Setup

### Prerequisites

- Git
- Bash shell
- Node.js 18+ (for linting tools)

### Local Development

```bash
# Clone the repository
git clone https://github.com/FutureTranz-Inc/ai-ethics.git
cd ai-ethics

# Install development tools
npm install -g markdownlint-cli yaml-lint

# Run linting
markdownlint '**/*.md'
yamllint **/*.yml

# Test scripts
bash scripts/ci-check-attribution.sh
```

## Code Style

- Use Markdown for documentation
- Use YAML for configuration files
- Follow shell script best practices
- Use descriptive variable names
- Add comments for complex logic

## Testing

- Test all shell scripts with `bash -n script.sh`
- Validate YAML files with `yamllint`
- Test git hooks manually
- Ensure CI workflows pass

## Documentation

- Update README.md for new features
- Add examples for new scripts
- Keep CHANGELOG.md current
- Document configuration options

## Community

- Join discussions in Issues
- Be respectful and constructive
- Help other contributors
- Share your use cases

## Recognition

Contributors will be recognized in:

- CHANGELOG.md
- Repository contributors list
- Release notes

Thank you for helping make AI more ethical and accountable! 🚀
