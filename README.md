# Sphinx Deploy to GH-Pages Action

This action builds and deploys a Sphinx site to the `gh-pages` branch.

## Usage

Create a new GitHub Actions workflow in your Sphinx project repository and add the following configuration:

```yaml
name: Build and Deploy Sphinx

on:
  push:
    branches:
      - main  # or master, depending on your default branch name

jobs:
  build-and-deploy:
    runs-on: ubuntu-latest

    steps:
    - name: Checkout repository
      uses: actions/checkout@v2

    - name: Build and Deploy Sphinx site
      uses: photon-platform/action-deploy-sphinx-gh-pages@v1
      with:
        python_version: '3.x'  # Optional, default is '3.x'
```
