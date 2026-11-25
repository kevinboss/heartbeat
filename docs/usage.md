# Usage

## Sending a manual beat

At 00:00 UTC each day, Heartbeat checks `beats.yaml` for repositories whose
last recorded activity is more than 30 days old. When a repository passes that
threshold, Heartbeat opens an issue titled
`Request heartbeat for <owner>/<name>` assigned to the repository owner.

Reply to the issue with a comment containing only `#beat`. Heartbeat records
the comment timestamp in `beats.yaml` and deletes the issue.

## Badge states

At 01:00 UTC each day, Heartbeat regenerates `badges/<owner>_<name>.svg` from
the timestamp in `beats.yaml`:

- `strong` (green): last commit or beat is 30 days old or newer.
- `weak` (orange): last commit or beat is 31 to 60 days old.
- `none` (red): no beat recorded, or last activity is over 60 days old.

## Self-hosting

To run Heartbeat in your own fork, replace the files in `hearts/` with your own
repositories. Give GitHub Actions workflows write permissions so they can
commit updates to `beats.yaml` and `badges/`, and add a repository secret named
`ACCESS_TOKEN` so the beat workflow can delete resolved prompt issues.
