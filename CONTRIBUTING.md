# Contributing

## Setup

Install [Git](https://git-scm.com/doc) and fork the repository. Heartbeat has
no build step or local test suite; its automation lives in
[GitHub Actions](https://docs.github.com/en/actions) workflows under
`.github/workflows/`, which use [`jq`](https://jqlang.org/manual/) and
[`yq`](https://mikefarah.gitbook.io/yq/).

## Testing and pull requests

To test workflow changes, run `check.yaml`, `ask.yaml`, or `generate.yaml`
manually from your fork's Actions tab via `workflow_dispatch`, then open an
issue or pull request.
