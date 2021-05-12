# appreciation-engine-whitelist

You can use this Github-Action to add or remove domains from Appreciation Engine's whitelist.

The following workflow is an example a domain is added to the whitelist.

### .github/workflows/main.yml
```
on: [push]

jobs:
  appreciation-engine-whitelist:
    runs-on: ubuntu-latest
    name: Add domain to whitelist
    steps:
    - uses: actions/checkout@v2
    - id: ae-whitelist
      uses: actions/appreciation-engine-whitelist@v1
      with:
        operation: 'whitelist'
        environment: 'staging'
        domain: 'example.com'
        apiKey: "asoifh083h20r8hf0a"
```