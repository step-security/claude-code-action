[![StepSecurity Maintained Action](https://raw.githubusercontent.com/step-security/maintained-actions-assets/main/assets/maintained-action-banner.png)](https://docs.stepsecurity.io/actions/stepsecurity-maintained-actions)

![Claude Code Action responding to a comment](https://github.com/user-attachments/assets/1d60c2e9-82ed-4ee5-b749-f9e021c85f4d)

# Claude Code Action

A general-purpose [Claude Code](https://claude.ai/code) action for GitHub PRs and issues that can answer questions and implement code changes. This action intelligently detects when to activate based on your workflow context—whether responding to @claude mentions, issue assignments, or executing automation tasks with explicit prompts. It supports multiple authentication methods including Anthropic direct API, Amazon Bedrock, and Google Vertex AI.

## Features

- 🎯 **Intelligent Mode Detection**: Automatically selects the appropriate execution mode based on your workflow context—no configuration needed
- 🤖 **Interactive Code Assistant**: Claude can answer questions about code, architecture, and programming
- 🔍 **Code Review**: Analyzes PR changes and suggests improvements
- ✨ **Code Implementation**: Can implement simple fixes, refactoring, and even new features
- 💬 **PR/Issue Integration**: Works seamlessly with GitHub comments and PR reviews
- 🛠️ **Flexible Tool Access**: Access to GitHub APIs and file operations (additional tools can be enabled via configuration)
- 📋 **Progress Tracking**: Visual progress indicators with checkboxes that dynamically update as Claude completes tasks
- 🏃 **Runs on Your Infrastructure**: The action executes entirely on your own GitHub runner (Anthropic API calls go to your chosen provider)
- ⚙️ **Simplified Configuration**: Unified `prompt` and `claude_args` inputs provide clean, powerful configuration aligned with Claude Code SDK

## Quickstart

### Option 1: Manual Setup (Recommended for StepSecurity Maintained Action)

**To use this action in your own repository:**

1. Choose a workflow template from the [Ready-to-Use Examples](#-ready-to-use-workflow-examples) below
2. Copy it to your `.github/workflows/` directory
3. Add your `ANTHROPIC_API_KEY` to repository secrets
4. Customize triggers and permissions as needed

## 🔧 Ready-to-Use Workflow Examples

Copy any of these complete workflow examples to your `.github/workflows/` directory:

### Core Workflows

- **[`claude.yml`](./examples/claude.yml)** - Basic Claude interaction with `@claude` mentions
- **[`issue-triage.yml`](./examples/issue-triage.yml)** - Automatic issue labeling when issues are created

### PR Review Automation

- **[`pr-review-comprehensive.yml`](./examples/pr-review-comprehensive.yml)** - Complete PR analysis with inline comments
- **[`pr-review-filtered-authors.yml`](./examples/pr-review-filtered-authors.yml)** - Review only PRs from specific authors
- **[`pr-review-filtered-paths.yml`](./examples/pr-review-filtered-paths.yml)** - Review only when specific files/directories change

### Issue Management

- **[`issue-deduplication.yml`](./examples/issue-deduplication.yml)** - Detect and manage duplicate issues

### CI/CD Integration

- **[`ci-failure-auto-fix.yml`](./examples/ci-failure-auto-fix.yml)** - Automatically analyze and suggest fixes for CI failures
- **[`manual-code-analysis.yml`](./examples/manual-code-analysis.yml)** - On-demand code quality analysis

### Option 2: Original Anthropic Setup

Alternatively, you can use the original setup method through [Claude Code](https://claude.ai/code) terminal with `/install-github-app`, but this will install the original `anthropics/claude-code-action`.

**Note**:

- You must be a repository admin to install GitHub apps and add secrets
- For AWS Bedrock or Google Vertex AI setup, see [docs/cloud-providers.md](./docs/cloud-providers.md)

## 📚 Solutions & Use Cases

Looking for specific automation patterns? Check our **[Solutions Guide](./docs/solutions.md)** for complete working examples including:

- **🔍 Automatic PR Code Review** - Full review automation
- **📂 Path-Specific Reviews** - Trigger on critical file changes
- **👥 External Contributor Reviews** - Special handling for new contributors
- **📝 Custom Review Checklists** - Enforce team standards
- **🔄 Scheduled Maintenance** - Automated repository health checks
- **🏷️ Issue Triage & Labeling** - Automatic categorization
- **📖 Documentation Sync** - Keep docs updated with code changes
- **🔒 Security-Focused Reviews** - OWASP-aligned security analysis
- **📊 DIY Progress Tracking** - Create tracking comments in automation mode

Each solution includes complete working examples, configuration details, and expected outcomes.

## Documentation

- **[Solutions Guide](./docs/solutions.md)** - **🎯 Ready-to-use automation patterns**
- **[Migration Guide](./docs/migration-guide.md)** - **⭐ Upgrading from v0.x to v1.0**
- [Setup Guide](./docs/setup.md) - Manual setup, custom GitHub apps, and security best practices
- [Usage Guide](./docs/usage.md) - Basic usage, workflow configuration, and input parameters
- [Custom Automations](./docs/custom-automations.md) - Examples of automated workflows and custom prompts
- [Configuration](./docs/configuration.md) - MCP servers, permissions, environment variables, and advanced settings
- [Experimental Features](./docs/experimental.md) - Execution modes and network restrictions
- [Cloud Providers](./docs/cloud-providers.md) - AWS Bedrock and Google Vertex AI setup
- [Capabilities & Limitations](./docs/capabilities-and-limitations.md) - What Claude can and cannot do
- [Security](./docs/security.md) - Access control, permissions, and commit signing
- [FAQ](./docs/faq.md) - Common questions and troubleshooting

## 📚 FAQ

Having issues or questions? Check out our [Frequently Asked Questions](./docs/faq.md) for solutions to common problems and detailed explanations of Claude's capabilities and limitations.

## License

This project is licensed under the MIT License—see the LICENSE file for details.
