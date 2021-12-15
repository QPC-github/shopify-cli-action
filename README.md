<div align="center">
  <img src="assets/logo.png" width="150"/>
  <h1>Shopify CLI Action</h1>
</div>


This repository contains a [GitHub Action](https://github.com/features/actions) to use the Shopify CLI from CI pipelines.


## Usage

```yaml
name: My project

on:
  push:
    branches:
      - main
  pull_request:

jobs:
  build:
    name: Build
    runs-on: macos-latest
    steps:
      - uses: actions/checkout@v1
      - uses: tuist/shopify-cli-action@0.1.0
        with:
          command: 'script push'
```