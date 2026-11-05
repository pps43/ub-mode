# Upstream sync

This fork checks `unclebob/ub-mode:master` on the first day of each month and can also be run manually from the Actions tab. When upstream has new commits, the workflow merges them into a dated `automation/upstream-sync-YYYY-MM` branch and opens or updates a pull request against this fork's `master` branch.

The workflow does not merge the pull request. Review the changes and merge it manually. If Git cannot merge upstream cleanly, the run fails before pushing a branch; resolve the conflict in a separate branch and open a PR yourself.

GitHub Actions is enabled for this fork, and the repository is configured to let Actions create pull requests. The workflow requests only `contents: write` and `pull-requests: write` for its built-in `GITHUB_TOKEN`; the repository-wide default token permissions remain read-only.
