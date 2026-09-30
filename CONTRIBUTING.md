# Contributing

Thank you for your interest in contributing to this project! This guide applies to this
repository and other Lamassu Open Source repositories that follow the same workflow.

## Code of Conduct

This project and everyone participating in it is governed by our [Code of Conduct](./CODE_OF_CONDUCT.md).

## Contributor License Agreement

Before a contribution can be accepted, the contributor must use the agreement that matches the
capacity in which the contribution is made:

- Individual contributors acting solely on their own behalf must accept the ICLA.
- Contributions made by employees, contractors, or other representatives of an organization
  must be covered by the organization's CCLA.
- A contribution covered by a CCLA must not also be submitted under the ICLA.
- The ICLA and CCLA text, current versions, and signing instructions are maintained centrally in
  the Lamassu platform repository.

Read the current agreements and signing instructions:

- [Lamassu legal documentation](https://github.com/lamassuiot/lamassu-platform/tree/main/legal)
- [ICLA and CCLA](https://github.com/lamassuiot/lamassu-platform/tree/main/legal/cla)

Signed agreements, contributor identity data, corporate authorization evidence, and other private
legal records must not be committed to this repository or submitted through public issues or pull
requests.

CLA verification is mandatory before merging, in addition to normal code review and required
status checks. Maintainers follow the [manual verification process](https://github.com/lamassuiot/lamassu-platform/tree/main/legal/cla-maintainer-runbook.md).

## Workflow overview

Strategic planning is managed centrally. Implementation work is created in this
repository as **Features**, **Tasks**, or **Bugs**. All changes are submitted through
**Pull Requests**.

```
Strategic initiative → Feature / Task / Bug → Branch → Pull Request → Review → Merge
```

Please create or link an issue before starting implementation work.

## Reporting bugs

1. Search existing issues to avoid duplicates.
2. Open a new issue using the **Bug** form.
3. Include clear reproduction steps, expected vs. actual behavior, and your environment.
4. Do **not** include credentials, tokens, private keys, or customer-identifiable data.
5. If you believe you've found a security vulnerability, follow [SECURITY.md](./SECURITY.md)
   instead of filing a public issue.

## Requesting features

Open a new issue using the **Feature** form. Describe the problem or motivation,
your proposed solution, and any alternatives you considered.

## Creating implementation issues

Use the **Task** form for well-scoped, actionable implementation work. Include the
objective, scope, and acceptance criteria.

## Branch naming

Use a short, descriptive branch name prefixed by the type of change, for example:

```
feature/<short-description>
task/<short-description>
bugfix/<short-description>
```

## Commit messages and PR titles

This repository uses [git-cliff](https://git-cliff.org/) (see [`cliff.toml`](./cliff.toml)) to
generate [`CHANGELOG.md`](./CHANGELOG.md) from commit history, based on
[Conventional Commits](https://www.conventionalcommits.org/). Format your commit messages (or
your pull request title, if this repository squash-merges pull requests) as:

```
<type>[optional scope]: <description>
```

Common types: `feat`, `fix`, `docs`, `style`, `refactor`, `perf`, `test`, `build`, `ci`, `chore`.
Pull request titles are checked automatically by CI against this format.

## Pull requests

* Keep PRs small, focused, and reviewable.
* Fill out the [pull request template](./.github/pull_request_template.md) completely.
* Reference the issue the PR addresses (e.g. `Closes #123`).
* Ensure CI checks pass before requesting review.

## Review expectations

* At least one maintainer review is required before merging.
* Reviewers may request changes; please respond to all review comments.
* Be respectful and constructive — see our [Code of Conduct](./CODE_OF_CONDUCT.md).
* See [CODEOWNERS](./.github/CODEOWNERS) for who is required to review changes in this repository.

## Tests and documentation

* Add or update tests for any behavioral change.
* Update relevant documentation (README, code comments, etc.) alongside code changes.

## Avoiding secrets and confidential information

Never commit credentials, tokens, private keys, customer data, internal URLs, or other
confidential information. If you accidentally commit a secret, notify a maintainer
immediately so it can be rotated and removed from history.

## Referencing an issue

Use GitHub's closing keywords in your PR description to link work to its issue, for example:

```
Closes #123
Fixes #123
Relates to #123
```

## Repository governance

This repository may be protected by GitHub branch protection rules or rulesets (for example,
required reviews from [CODEOWNERS](./.github/CODEOWNERS), required status checks, or commit
signing). Direct commits to protected branches are not allowed — always submit changes through
Pull Requests. Verify the current protection rules configured on GitHub rather than assuming
those described here, since governance may evolve as the project and maintainer team grow.
