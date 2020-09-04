# GitHub Action: Ktlint

Cli tools for using ktlint in github actions

## Example

```yaml
name: ktlint

on:
  push:
    branches: [ master ]

 jobs:
   ktlint:
     runs-on: ubuntu-latest

     steps:
       - name: checkout
         uses: actions/checkout@v2
       - name: ktlint
         uses: lionzxy/ktlint@0.38.1
```

## Usage with CLI

```yaml
name: ktlint

on:
  push:
    branches: [ master ]

 jobs:
   ktlint:
     runs-on: ubuntu-latest

     steps:
       - name: checkout
         uses: actions/checkout@v2
       - name: ktlint
         uses: lionzxy/ktlint@0.38.1
         with:
          args: --reporter=checkstyle,output=build/ktlint-report-in-checkstyle-format.xml
```
