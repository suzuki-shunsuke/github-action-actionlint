# github-action-actionlint

GitHub Actions for actionlint

Run actionlint and notify the result with reviewdog.
This GitHub Actions does **not** install actionlint and reviewdog, so you have to install them in advance.
It allows to install tools outside this action.
We recommend [aqua](https://aquaproj.github.io/) to install them.

## Motivation

We know there are other GitHub Actions for actionlint.
They install actionlint automatically, but we would like to manage tools with [aqua](https://aquaproj.github.io/), which is a declarative CLI Version Manager written in Go.
By aqua, you can update tools continuously with Renovate very easily and use the same tool versions in both CI and your development environment.
This GitHub Actions does **not** install actionlint, so we can install them outside this action.

## Requirements

* [actionlint](https://github.com/rhysd/actionlint)
* [reviewdog](https://github.com/reviewdog/reviewdog)

## Example

```yaml
- uses: suzuki-shunsuke/github-action-actionlint@v0.1.2
```

```yaml
- uses: suzuki-shunsuke/github-action-actionlint@v0.1.2
  with:
    github_token: ${{ secrets.GITHUB_TOKEN }}
```

## Inputs

### Required Inputs

Nothing.

### Optional Inputs

name | default value | description
--- | --- | ---
github_token | `github.token` | GitHub Access Token

## Outputs

Nothing.

## License

[MIT](LICENSE)
