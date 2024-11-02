# public-reusable-workflows

This repository contains a set of reusable workflows for GitHub Actions that can be easily imported and used in various projects.

## Contents

- Ready-to-use workflows for automating CI/CD processes
- Usage and configuration examples
- Easy integration with other repositories

## How to use

1. In your repository, create a workflow file in `.github/workflows/`.
2. Use `workflow_call` to invoke a workflow from this repository.

Example usage in a workflow file:

```yaml
name: Example CI

on:
  push:
    branches: [main]

jobs:
  ci:
    uses: moose96/public-reusable-workflows/.github/workflows/ci.yml@main
    with:
      # input parameters, if required
    secrets:
      # secrets, if required
```

## Requirements

- GitHub Actions
- Appropriate permissions to call workflows from another repository
