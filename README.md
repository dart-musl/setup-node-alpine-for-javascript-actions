# setup-node-alpine-for-javascript-actions

[![build](https://github.com/dart-musl/setup-node-alpine-for-javascript-actions/actions/workflows/build.yml/badge.svg)](https://github.com/dart-musl/setup-node-alpine-for-javascript-actions/actions/workflows/build.yml)

This action fixes the following error for GitHub Actions users:

> JavaScript Actions in Alpine containers are only supported on x64 Linux runners.

## Usage

> [!CAUTION]  
> This action will change `ID=alpine` to `ID=linux` in `/etc/os-release`, which may break os detection for certain applications.   

``` yaml
jobs:
  build:
    runs-on: ubuntu-24.04-arm
    container:
      image: alpine
    steps:
      - uses: dart-musl/setup-node-alpine-for-javascript-actions@v1
```
