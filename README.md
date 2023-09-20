# Add Labels

A GitHub Action to add labels on PR / Issue events

Forked from christianvuerings/add-labels with https://github.com/christianvuerings/add-labels/pull/1 fix from @FDiskas

## Inputs

### `labels`

**Required** Labels to add.

## Example usage

```
name: Add Label
on:
  pull_request:
    branches:
      - master
    types:
      - opened

jobs:
  add-label:
    name: Add Label
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v2
      - uses: MakarovAleksey/add-labels@v1
        with:
          labels: |
            minor release
            bug
        env:
          GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }}
```

## Update compiled files

```
npm i
npm i -g @zeit/ncc
ncc build index.js
```
