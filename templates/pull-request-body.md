## Fixed code style violations with `sbt scalafmtAll`.

Code with non-conforming style was found on the default branch.
All violations have been fixed using `sbt scalafmtAll`.

### Trigger

This pull request was triggered by commit [$GITHUB_SHA](https://github.com/$GITHUB_REPOSITORY/commit/$GITHUB_SHA),
which introduced code style violations to the default branch.

### Explanation

This project uses [Scalafmt](https://scalameta.org/scalafmt/) to ensure that all code adheres to the style rules specified in [.scalafmt.conf](.scalafmt.conf).
