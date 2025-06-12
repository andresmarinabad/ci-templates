# 🚀 CI Templates

Centralized repository of **reusable CI/CD workflows** for GitHub Actions.  
Designed to standardize and simplify automation across multiple projects.

---

## 📦 Contents

This repository contains **reusable workflows** (`workflow_call`) that can be imported and used in any compatible project without duplicating logic.

### Available Workflows

| Name                    | Description                                            |
|-------------------------|--------------------------------------------------------|

---

## 🛠️ Usage

To use a workflow from this repository in your own project:

```yaml
# .github/workflows/ci.yml in your project
name: CI

on: [push, pull_request]

jobs:
  test:
    uses: your-org/ci-templates/.github/workflows/test.yml@main
    with:
      node-version: '20'
```

## 🧱 Requirements
GitHub Actions enabled
If your repository is private, ensure you configure the appropriate workflow permissions
Your project should match the expected structure (e.g., use npm, Dockerfile, etc.)

## ➕ Adding New Workflows
Create a new file under .github/workflows/.
Use workflow_call to make it reusable.
Follow the input and secret naming conventions.
Open a pull request and update this README with the new workflow.
