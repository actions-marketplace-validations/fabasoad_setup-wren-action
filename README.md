# Setup wren
![GitHub release](https://img.shields.io/github/v/release/fabasoad/setup-wren-action?include_prereleases) ![CI (latest)](https://github.com/fabasoad/setup-wren-action/workflows/CI%20(latest)/badge.svg) ![CI (main)](https://github.com/fabasoad/setup-wren-action/workflows/CI%20(main)/badge.svg) ![YAML Lint](https://github.com/fabasoad/setup-wren-action/workflows/YAML%20Lint/badge.svg) [![Total alerts](https://img.shields.io/lgtm/alerts/g/fabasoad/setup-wren-action.svg?logo=lgtm&logoWidth=18)](https://lgtm.com/projects/g/fabasoad/setup-wren-action/alerts/) [![Language grade: JavaScript](https://img.shields.io/lgtm/grade/javascript/g/fabasoad/setup-wren-action.svg?logo=lgtm&logoWidth=18)](https://lgtm.com/projects/g/fabasoad/setup-wren-action/context:javascript) [![Maintainability](https://api.codeclimate.com/v1/badges/e259e98506d3691ab916/maintainability)](https://codeclimate.com/github/fabasoad/setup-wren-action/maintainability) [![Known Vulnerabilities](https://snyk.io/test/github/fabasoad/setup-wren-action/badge.svg?targetFile=package.json)](https://snyk.io/test/github/fabasoad/setup-wren-action?targetFile=package.json)

This action sets up a [wren](https://github.com/wren-lang/wren-cli).

## Inputs
| Name    | Required | Description                                                                           | Default | Possible values |
|---------|----------|---------------------------------------------------------------------------------------|---------|-----------------|
| version | Yes      | wren version that can be found [here](https://github.com/wren-lang/wren-cli/releases) |         | &lt;String&gt;  |

## Example usage

### Workflow configuration

```yaml
name: Setup wren

on: push

jobs:
  setup:
    name: Setup
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v1
      - uses: fabasoad/setup-wren-action@main
        with:
          version: {PROJECT_VERSION}
      - name: Run script
        run: {EXAMPLE}
```

### Result
