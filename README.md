<div align="center">
  <h1>🔫Scalafmt Revolver</h1>
  <p>A tool to automatically fix <a href="https://scalameta.org/scalafmt/">Scalafmt</a> violations.</p>
</div>

## 💡 Overview

Scalafmt is a popular linter for ensuring that Scala code lives up to project-dependent style rules,
and then automatically fixing it when it doesn't.
_Scalafmt Revolver_ provides Scalafmt with GitHub integration,
which includes automated correction of violations.

## ⬇️ Installation

### 1. Add the linter workflow

Create a new workflow definition in `.github/workflows/linter.yml`:

```yaml
# linter.yml

name: Linter
on:
  pull_request:
    branches: [ main ]
  push:
    branches: [ main ]
  workflow_dispatch:
  workflow_call:

jobs:
  lint:
    uses: SgtSwagrid/scalafmt-revolver/linter.yml@main
    secrets:
      GITHUB_TOKEN: ${{ secrets.GH_TOKEN }}
```

### 2. Create a Personal Access Token

In order for GitHub Actions to automatically commit fixes and manage pull requests,
you'll need a [Personal Access Token](https://docs.github.com/en/authentication/keeping-your-account-and-data-secure/managing-your-personal-access-tokens) (PAT) with at least the following permissions in your repository:
- `Contents` with access `Read and write`.
- `Pull requests` with access `Read and write`.

> **Note:** Without a PAT, the built-in `GITHUB_TOKEN` can still create PRs and commits,
> but those commits won't trigger further CI workflows due to a GitHub limitation.
> As such, this isn't supported here.

You can manage your tokens [here](https://github.com/settings/personal-access-tokens).

Once created, add it as a repository secret named `GH_TOKEN` under:
> **Settings → Secrets and variables → Actions → New repository secret**

## 🔨 Usage

Once installed, the linter runs automatically on every push and pull request targeting the default branch.
No further configuration is required beyond having a `.scalafmt.conf` in your repository.

If a formatting violation is detected:
- On a **pull request**, the fix is committed directly to the PR branch and the workflow passes.
- On a **push to main**, a new pull request (`scalafmt`) is opened with the fix applied.

The workflow can also be triggered manually from the **Actions** tab using `workflow_dispatch`.

## 👁️ See also

- See [GitHub Graph](https://github.com/SgtSwagrid/github-graph) for a similar tool to duplicate files across multiple GitHub repositories.
- See [GitHub Rules](https://github.com/SgtSwagrid/github-rules) for a similar tool to define GitHub [rulesets](https://docs.github.com/en/repositories/configuring-branches-and-merges-in-your-repository/managing-rulesets/about-rulesets) in-source.
- This project is configured by [Git Config](https://github.com/SgtSwagrid/git-config).
