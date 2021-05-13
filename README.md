# appreciation-engine-whitelist

You can use this Github-Action to add or remove domains from Appreciation Engine's whitelist.

The following workflow adds an example domain to the whitelist.

### .github/workflows/main.yml
```
on: [push]

jobs:
  build:
    runs-on: ubuntu-latest
    name: Add domain to whitelist
    steps:
    - name: Add domain to whitelist
      uses: phantomstudios/appreciation-engine-whitelist@v0.0.1
      with:
        operation: whitelist
        environment: staging
        domain: example.com
        apiKey: 921f9u9ooDUMMYKEYoo3h08h
```
