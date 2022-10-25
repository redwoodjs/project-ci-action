# project-action-ci

GitHub Action for RedwoodJS Project CI

## Example

The following tests and perform quality assurances on your project when a pull request is [opened, synchronized, or reopened](https://docs.github.com/en/actions/using-workflows/events-that-trigger-workflows#pull_request).

```YAML
# .github/workflows/qa.yaml
name: CI — Quality Assurance

on:
  pull_request:
    branches: [main]
    types: [opened, synchronize, reopened]
    paths-ignore:
      - README.md
      - .vscode/**

jobs:
  qa:
    runs-on: ubuntu-latest
    steps:
      - name: RedwoodJS - Build, Lint, Diagnostics, and Tests
        uses: redwoodjs/project-ci-action@v0.1.1
```
