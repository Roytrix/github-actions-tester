# GitHub Actions Workflow Development Guide with Copilot

This guide provides instructions for using GitHub Copilot to create efficient GitHub Actions workflows with Bash scripting and GitHub CLI integration.

## Workflow Structure Best Practices

When asking Copilot to generate a GitHub Actions workflow:

- Request a clear name and description for the workflow
- Specify trigger events (push, pull_request, schedule, etc.)
- Define environment variables at the top of the workflow
- Use reusable workflows for common patterns
- Include proper error handling and notifications

Example prompt:
```
Generate a GitHub Actions workflow that runs linting and tests on PRs to the main branch. 
Use a matrix strategy for multiple Node.js versions.
```

## Bash Scripting in GitHub Actions

When writing Bash scripts for GitHub Actions:

- Always start with proper shebang: `#!/bin/bash`
- Set `-e` (exit on error) and `-o pipefail` flags
- Use explicit error messages with appropriate exit codes
- Leverage GitHub's environment variables
- Prefer multi-line scripts with proper indentation for complex operations

Example prompt:
```
Create a bash script for a GitHub Action step that checks for security vulnerabilities 
in dependencies and posts results as a PR comment.
```

## GitHub CLI Integration 

When using GitHub CLI (gh) in workflows:

- Ensure proper authentication with `gh auth`
- Use GitHub token for authentication: `${{ secrets.GITHUB_TOKEN }}`
- Chain commands for efficiency
- Format output for readability
- Handle rate limiting with proper error checking

Example prompt:
```
Create a workflow step using GitHub CLI to automatically label PRs based on file changes.
```

## Security Considerations

Ask Copilot to implement these security practices:

- Minimize using third-party actions
- Pin action versions with SHA hashes
- Use least privilege principle for tokens and permissions
- Implement proper secret handling
- Add timeout limits to prevent runaway workflows

Example prompt:
```
Modify this workflow to follow security best practices with minimal permissions and proper
secret handling.
```

## Complete Workflow Examples

Ask Copilot for complete workflow examples:

```
Generate a GitHub Actions workflow that:
1. Builds a Docker image
2. Runs tests
3. Publishes to GitHub Container Registry if on main branch
4. Creates a release with changelog when tagged
5. Uses GitHub CLI to notify a Slack channel on failure
```

## Advanced Techniques

For complex workflows, request:

- Workflow dispatch inputs for manual triggers
- Composite actions for reusable components
- Matrix strategies for parallel testing
- Job dependencies with proper artifact passing
- Custom environment deployment logic

Example prompt:
```
Create a workflow that implements a progressive deployment strategy with GitHub
environments, approval gates, and automatic rollback on failure.
```

## Debugging Tips

For better debugging, ask Copilot to include:

- Verbose logging flags
- Strategy to use GitHub's debugging features
- Self-hosted runner setup if needed
- Workflow visualization with dependency graphs
- Caching strategies for faster runs

Example prompt:
```
Add comprehensive debugging and logging to this workflow to help diagnose intermittent failures.
```