<div align="center">
  <h1>🔫Scalafmt Revolver</h1>
  <p>A tool to automatically fix <a href="https://scalameta.org/scalafmt/">Scalafmt</a> violations.</p>
</div>

## 💡 Overview

Scalafmt is a popular linter for ensuring that Scala code lives up to project-dependent style rules,
and then automatically fixing it when it doesn't.
_Scalafmt Revolver_ provides Scalafmt with GitHub integration.
This includes:
- When a pull request targeting the default branch fails the lint check, the code is fixed by an automatic workflow.
- When the default branch itself fails the lint check, a new pull request is opened to fix this.

## ⬇️ Installation

### 1. ???

### 2. Create a Personal Access Token

In order for GitHub Actions to automatically manage pull requests,
you'll need a [Personal Access Token](https://docs.github.com/en/authentication/keeping-your-account-and-data-secure/managing-your-personal-access-tokens) (PAT) with at least the following permissions in your repository:
- `Contents` with access `Read and write`.
- `Pull requests` with access `Read and write`.

You can manage your tokens [here](https://github.com/settings/personal-access-tokens).
Once created, add it as a repository secret named `GH_TOKEN` under:
> **Settings → Secrets and variables → Actions → New repository secret**

## 👁️ See also

- See [GitHub Graph](https://github.com/SgtSwagrid/github-graph) for a similar a tool to duplicate files across multiple GitHub repositories.
- See [GitHub Rules](https://github.com/SgtSwagrid/github-rules) for a similar tool to define GitHub [rulesets](https://docs.github.com/en/repositories/configuring-branches-and-merges-in-your-repository/managing-rulesets/about-rulesets) in-source.
- This project is configured by [Git Config](https://github.com/SgtSwagrid/git-config).
