# scala-cla
Checks if the author has signed the Scala CLA

Usage
-----

Here's an example that checks if author of Pull Requests had signed Scala CLA.

```yaml
name: "Check Scala CLA"
on:
  pull_request:
jobs:
  cla-check:
    runs-on: ubuntu-latest
    steps:
      - name: Verify CLA
        uses: scala/cla-checker
        with:
          author: ${{ github.event.pull_request.user.login }}
```
