# E-Commerce Shared Pipelines

Reusable GitHub Actions workflows and templates for the E-Commerce platform.

## Available Workflows

- **dotnet-ci.yml** - .NET CI pipeline with testing and security scanning
- **docker-build.yml** - Docker image build and push
- **deploy-azure.yml** - Azure deployment pipeline
- **quality-gates.yml** - Code quality and architecture validation
- **angular-ci.yml** - Angular frontend CI pipeline

## Usage

Reference these workflows in your repository:

```yaml
jobs:
  ci:
    uses: smartsolutionslab/e-commerce-shared-pipelines/.github/workflows/dotnet-ci.yml@main
    with:
      dotnet-version: '9.0.x'
      run-tests: true
    secrets: inherit
```

## Secrets Required

- `GITHUB_TOKEN` - GitHub token for package registry
- `AZURE_CREDENTIALS` - Azure service principal credentials
- `SONAR_TOKEN` - SonarCloud token for code analysis
