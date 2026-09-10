# .github

## Reusable workflows

### `common-ci.yaml`

The reusable Common CI workflow keeps the existing main-branch publishing behavior and now also supports opt-in image publishing for pull requests.

- Pushes from `main` continue to publish the `latest` image tag.
- Pull request runs publish only when the PR includes the configured trigger label.
- Labeled pull request images are published with the tag format `feature-pr-<PR number>` so they never overwrite `latest`.

The reusable workflow accepts an optional `feature-build-label` input and defaults it to `feature`.

Example caller trigger:

```yaml
on:
  push:
    branches:
      - main
  pull_request:
    types:
      - opened
      - reopened
      - synchronize
      - labeled
      - unlabeled
```

Example caller usage:

```yaml
jobs:
  ci:
    uses: its-the-vibe/.github/.github/workflows/common-ci.yaml@main
    with:
      feature-build-label: feature
```
