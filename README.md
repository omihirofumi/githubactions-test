# GitHub Actions Test

This repository contains sample GitHub Actions workflows.

## Workflows

### CI Workflow (`ci.yml`)

This workflow runs on push to `main`/`master` branches and on pull requests to those branches. It performs the following steps:

- Checks out the code
- Sets up Node.js (versions 16.x, 18.x, and 20.x)
- Installs dependencies
- Runs linting
- Runs tests
- Builds the project

### Release Workflow (`release.yml`)

This workflow runs when you push a tag that starts with `v` (e.g., `v1.0.0`). It performs the following steps:

- Checks out the code
- Sets up Node.js
- Installs dependencies
- Builds the project
- Runs tests
- Creates a GitHub Release
- (Optional) Publishes to npm (needs to be uncommented and configured)

## How to Use

1. Push code to the `main` or `master` branch to trigger the CI workflow.
2. Create and push a tag starting with `v` to trigger the release workflow:

```bash
git tag v1.0.0
git push origin v1.0.0
```

## Configuration

You may need to customize these workflows based on your specific project needs:

- Update the Node.js versions if needed
- Modify or remove steps that don't apply to your project
- Add environment-specific variables or secrets
