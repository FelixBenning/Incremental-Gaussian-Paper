# article-template

LaTeX template for an article

## GitHub Actions

- Every Commit to a Branch with an Active Pull Request to `main` is tested (i.e.
the GitHub action attempts to compile the pdf. The result is attached to the
workflow run as an artifact)
- Every Commit to the `main` branch, results in a Release. To make this release,
the action tags the latest commit using the current date. For the Release title
the first line of the commit message is used. For the Release body, the body
of the commit message is used.

> If you merge with a `rebase`, the release mechanism does not work as well,
since the last commit message won't be as meaningful. It is therefore advisable
to either `squash` or `merge` pull requests.

## ArXiv compatible

The name of the main file is `ms.tex` as ArXiv suggests for the top file.