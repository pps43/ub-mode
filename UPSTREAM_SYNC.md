# Upstream sync

This fork checks `unclebob/ub-mode:master` on the first day of each month and can also be run manually from the Actions tab. When upstream has new commits, the workflow merges them into a dated `automation/upstream-sync-YYYY-MM` branch and opens or updates a pull request against this fork's `master` branch.

The workflow does not merge the pull request. Review the changes and merge it manually. If Git cannot merge upstream cleanly, the run fails before pushing a branch; resolve the conflict in a separate branch and open a PR yourself.

After creating a fork, GitHub may require Actions to be enabled for that fork. In the repository's Actions settings, allow GitHub Actions and set workflow permissions to read and write so the built-in `GITHUB_TOKEN` can push the sync branch and open a pull request.
