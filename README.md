# reusable-workflows

[![GitHub tag](https://img.shields.io/github/tag/interlok-tooling/reusable-workflows.svg)](https://github.com/interlok-tooling/reusable-workflows/tags) ![license](https://img.shields.io/github/license/interlok-tooling/reusable-workflows.svg)

Reusable GitHub worfklows:

- **gradle-publish**: Gradle workflow to build and publish Interlok optional components nightly and on push on develop
- **gradle-check.yml**: Gradle workflow to build and check Interlok optional components on push to branches
- **gradle-check-test-project.yml**: Gradle workflow to build and check test projects
- **approve-merge-dependabot-pr.yml**: Workflow to auto approve and merge some dependabot dependencies upgrade PRs

The three Gradle workflows accept an optional `java-version` input. It defaults to
`'17'` and accepts versions supported by `actions/setup-java`. For example:

```yaml
jobs:
  gradle-check:
    uses: interlok-tooling/reusable-workflows/.github/workflows/gradle-check.yml@main
    with:
      java-version: '21'
    secrets:
      # secret secrets
```
