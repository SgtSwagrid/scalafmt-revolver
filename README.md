<div align="center">
  <h1>⚙️ Git Config</h1>
  <p>The single source of truth for basic configuration across many of my projects on GitHub.</p>
</div>

## 👷 What's the workflow?

Changes made to the configuration files contained herein are automatically copied into each dependent project using [GitHub Graph](https://github.com/SgtSwagrid/github-graph).
Updates to these files should be made _here_, not in any of the downstream repositories, lest they be overwritten later.

## 📋 What's included?

- Git settings including `.gitignore` and `.gitattributes`.
- Basic IDE configuration in `.editorconfig`.
- The [MIT](https://tlo.mit.edu/understand-ip/exploring-mit-open-source-license-comprehensive-guide) license,
  which I tend to use by default as it is fairly permissive.
- Configuration for [github-rules](https://github.com/SgtSwagrid/github-rule) to define GitHub rulesets in-source.
- [Claude Code](https://claude.com/product/claude-code) integration with GitHub.

## 🏗️ Where is this used?

The full list of projects that rely on this configuration is defined in [graph.json](.github/graph.json).

## 🤔 Should I use this in my projects too?

Only if you want to, but this exists mainly for my own convenience.
I would, however, argue that these settings are reasonable defaults for many projects.

## 🔨 How can this be used?

You have several options:

1. If you want continuous updates as this repository evolves, open a PR to add your project(s) to [graph.json](.github/graph.json).
   You'll also need to send me a [PAT](https://docs.github.com/en/authentication/keeping-your-account-and-data-secure/managing-your-personal-access-tokens) with write access to the corresponding repositories.
2. If you want continuous updates, but want to deviate from my template according to your own needs, fork this repository and _then_ add your project(s) to [graph.json](.github/graph.json) (after removing the existing projects from the list). In this case, you can add the PAT yourself.
3. If you just want the settings without the updates, click '**Use this template**' on GitHub (for a new project), or simply copy and paste the files (for an existing project).

## 👮‍♂️ License

The included MIT license should be considered only as part of the template, and is not binding.
This repository is hereby released to the public domain, to be used freely.
In particular, and contra [LICENSE.md](LICENSE.md), you may remove the license text from copies.

## 👁️ See also

- [Scala Config](https://github.com/SgtSwagrid/scala-config) is a downstream template for [Scala](https://www.scala-lang.org/) projects in particular.
