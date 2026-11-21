# Contributing

Small checkpoints. Evidence before progress.

## Workflow

1. Fork or create a focused topic branch from `main`.
2. Keep each pull request scoped to one logical fix, skill, or feature so diffs stay reviewable.
3. Run the repository local verification suite (`scripts/validate.py`, `npm test`, `pytest`, or `python3 -m unittest`) and include the command output in your pull request summary.
4. Check relative Markdown links and confirm no placeholder tokens or secrets appear in staged files.
5. Pin any new GitHub Actions workflow steps to full 40-character commit SHAs with explicit least-privilege `permissions`.

## Licensing

Unless a repository states a different license in its root `LICENSE` file, contributions are accepted under the same license as the target project.
