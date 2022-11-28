# .github

My Shared GitHub Actions & Configurations.

## Actions

tba

## Misc configurations

### Renovate config

Go through [the onboarding process](https://docs.renovatebot.com/getting-started/installing-onboarding/) and save the following snippet as `renovate.json` in the project root.

```json
{
  "$schema": "https://docs.renovatebot.com/renovate-schema.json",
  "extends": ["github>ivuorinen/.github:renovate-config"]
}

```
