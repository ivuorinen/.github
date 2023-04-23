# .github

My Shared GitHub Actions & Configurations.

## Actions

Actions should be linked using the `uses` keyword. Read more from the Reusing workflows article [Calling a reusable workflow](https://docs.github.com/en/actions/using-workflows/reusing-workflows#calling-a-reusable-workflow) and [jobs.<job_id>.steps[*].uses](https://docs.github.com/en/actions/using-workflows/workflow-syntax-for-github-actions#jobsjob_idstepsuses) configuration documentation.

```yml
jobs:
  CompressImages:
    uses: ivuorinen/.github/workflows/compress-images.yml

  ReusableMatrixJobForComposerInstall:
    strategy:
      matrix:
        target: ['8.0', '8.1', '8.2']
    uses: ivuorinen/.github/workflows/composer-install.yml@main
    with:
      php-versions: ${{ matrix.target }}
```

## Misc configurations

### Renovate config

Go through [the onboarding process](https://docs.renovatebot.com/getting-started/installing-onboarding/) and save the following snippet as `.github/renovate.json`.

```json
{
  "$schema": "https://docs.renovatebot.com/renovate-schema.json",
  "extends": ["github>ivuorinen/.github:renovate-config"]
}

```
