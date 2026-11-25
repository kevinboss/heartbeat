<p align="center">
  <img src="https://socialify.git.ci/kevinboss/heartbeat/image?font=Bitter&logo=https%3A%2F%2Fi.imgur.com%2FQOdFUxC.png&name=1&pattern=Solid&theme=Light" alt="Heartbeat">
</p>

<p align="center">
  A minimalist way for open-source maintainers to signal project vitality &mdash; a badge, not noise commits.
</p>

<p align="center">
  <a href="https://github.com/kevinboss/heartbeat/actions/workflows/generate.yaml"><img src="https://img.shields.io/github/actions/workflow/status/kevinboss/heartbeat/generate.yaml?label=CI" alt="CI"></a>
  <a href="LICENSE"><img src="https://img.shields.io/github/license/kevinboss/heartbeat" alt="License"></a>
</p>

Quiet repositories often leave users wondering whether a project is still
maintained. Heartbeat generates an SVG badge that communicates maintainer
activity without noise commits or feature updates. Each tracked repository is
configured with one YAML file, and GitHub Actions workflows track commits and
update the badge daily.

Add a YAML file in `hearts/` for your repository, such as
`hearts/your-repo.yaml`:

```yaml
owner: your-username
name: your-repo
```

Open a pull request to this repository, or fork it to host your own instance.
Once added, the daily workflows record your latest commit in `beats.yaml` and
write your badge to `badges/<owner>_<name>.svg` so you can display it in your
repository.

See [docs/usage.md](docs/usage.md) for manual beats, badge states, and
self-hosting.

## How to contribute

Fork the repository and test changes from your fork's Actions tab. See
[CONTRIBUTING.md](CONTRIBUTING.md) for tools, testing, and pull requests.
