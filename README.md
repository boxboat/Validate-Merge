# Validate Merge
This GitHub Action can enforce your branching policy. It can block Pull Requests from being merged to the wrong branch and provides guidance to developers on what merges are possible.

This action is intended to be used as a status check on Pull Requests.

After you implement this, your team will have guardrails to ensure they are merging from/to the correct branches.

## How To Use
Check out [.github/workflows/](.github/workflows/) for an example of how to use this.

All you need to do is create reference this action in your workflow and define the merges that you allow.

### Example
Allow merging `dev` to `test` and `test` to `main`.
```yaml
- name: Validate Merge
  uses: boxboat/Validate-Merge@0.0.1
  with:
    ACCEPTABLE_MERGES: |
      dev -> test
      test -> main
```
